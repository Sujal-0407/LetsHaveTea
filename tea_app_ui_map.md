# Tea Management App - UI / Layout Mapping

## 1. The Faculty (Member) View

**Goal:** Quick action. They should be able to open the app, log their status in 3 seconds, and see their money.

### Screen 1: The Daily Summary (Home Screen)
*   **Header:** Shows current date, e.g., "Monday, Oct 16".
*   **Big Number:** Their current available balance (e.g., `<Large Text> ₹450`).
    *   *If negative,* it turns red with "Pending Payment: ₹50".
*   **Today's Action Card:**
    *   Prompt: *"Did you drink tea today?"*
    *   Buttons: `[Absent]` `[No Tea]` `[1 Cup]` `[2 Cups]` `[Custom...]`
    *   Status Text: (e.g., *"Waiting for Leader to Approve"* or *"Approved: ₹15 Deducted"*).
*   **Footer Navigation:** `Home` \`|\` `History` \`|\` `Profile`

### Screen 2: History Tab
*   A clean list showing the last 30 days.
*   **Rows:** \`[Date]\` - \`[Action (e.g., 1 Cup)]\` - \`[-₹15 (Red)]\` or \`[+₹500 Deposit (Green)]\`.

---

## 2. The Leader (Admin) View

**Goal:** Total Control. A bird's-eye view of everyone's status and quick batch approvals.

### Screen 1: The Control Center (Home Screen)
*   **Header:** Shows current date and Total Group Balance (sum of all members' money).
*   **Alerts Section (Top):**
    *   "🔔 2 New members waiting to join" (Click to review/accept).
    *   "⚠️ 3 Faculties have negative balances" (Click to see who).
*   **Daily Approval Card (The most important part):**
    *   Input Field: `[Set Today's Tea Price: ₹___ ]`
    *   List of names below with their self-reported status right next to it:
        *   `John Doe: [ 1 Cup ]` (Editable dropdown)
        *   `Jane Smith: [ Absent ]` (Editable dropdown)
        *   `Bob Admin: [ No Entry ]` (Leader can change this to 1 cup if Bob forgot).
    *   **Big "Approve All" Button at the bottom.**

### Screen 2: Members Directory
*   A list of all faculties.
*   Next to each name: Their current balance.
*   Clicking a name brings up a `[Add Funds +]` button where the Leader types in the cash they received (e.g., +₹500).

### Screen 3: History & Reports Tab
*   Shows the history of every single day's approved totals (e.g., "Oct 16: 25 Cups - Total ₹375").
*   Export button to download an Excel sheet at the end of the month.
