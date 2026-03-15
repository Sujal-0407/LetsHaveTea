# Tea Management App - Blueprint

## Overview
A mobile application designed to manage a shared "Tea Fund" for college faculties. It acts as a digital ledger to track advance payments, daily tea consumption, and individual balances, all overseen by a designated Leader.

## 👥 User Roles & Permissions

### 1. The Leader (Admin)
*   **Group Management**: Creates the group and generates a "Secret Code" for faculties to join.
*   **Fund Management**: Manually adds advance money (e.g., ₹500, ₹1000) to individual faculty accounts when they pay in real life.
*   **Tea Pricing**: Decides and inputs the price of the tea for the current day (variable pricing).
*   **Verification & Approval**: Reviews the daily tea logs submitted by faculties and clicks "Approve" to officially deduct the money from their balances.

### 2. The Faculty (Member)
*   **Onboarding**: Downloads the app, creates a personal account, and joins the group using the Leader's Secret Code.
*   **Daily Logging**: Marks whether they drank tea (and how many cups) or if they are absent. Can also do this in advance for future days. **Note:** In case of errors or missed logs, the Leader can manually override and edit these entries.
*   **Balance Tracking**: Views their current available balance and transaction history. Balances can go negative, which will be displayed as a "Pending Payment" amount.
*   **Notifications**: Receives alerts when their balance drops low or goes into negative/pending status.

## 🔄 Core Workflows

1.  **Adding a Member**: 
    New Faculty signs up $\rightarrow$ Enters Secret Code $\rightarrow$ Leader receives a notification $\rightarrow$ Leader clicks "Accept" $\rightarrow$ Faculty appears in Leader's dashboard.
2.  **Topping Up Balance**: 
    Faculty pays Leader ₹500 in cash $\rightarrow$ Leader opens app $\rightarrow$ Adds ₹500 to Faculty's profile $\rightarrow$ Faculty receives notification.
3.  **Daily Tea Routine**: 
    *   Faculties mark their tea consumption for the day (e.g., "1 cup", "2 cups", or "Absent").
    *   Leader inputs today's tea price (e.g., ₹15 per cup).
    *   Leader reviews the list. If everything is correct, Leader clicks "Approve All".
    *   App calculates: (Cups consumed $\times$ ₹15) and deducts it from the respective balances.

## 🔒 Security & Trust
*   **Decentralized Entry but Centralized Approval**: To save the Leader time, faculties log their own consumption first. However, the final approval power rests solely with the Leader.
*   **No Blind Trust**: Faculties can claim they didn't drink tea, but the Leader must verify and approve the final data. If a faculty forgets to log, the Leader can add the entry for them.
*   **Secure Funds**: Faculties cannot artificially inflate their own balances; only the Leader has write-access to the funding ledger.
