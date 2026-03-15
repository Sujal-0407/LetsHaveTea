# Tea Management App - Notifications & Reminders

## 1. Automated "Nudges" (Daily Reminders)

To ensure the Leader doesn't have to chase people for data, the app should do the heavy lifting. **Note: The exact times for these nudges will be decided later and can be customized by the Leader in the settings.**

*   **The Daily Nudge (Faculties):** A daily push notification sent only to faculties who haven't logged their status for the day yet (e.g., at 4:00 PM).
    *   *Message:* "☕ Did you have tea today? Tap to log it so the Leader can approve!"
*   **The Daily Summary (Leader):** A notification to the Leader summarizing the day's readiness (e.g., at 5:30 PM).
    *   *Message:* "✅ 25/30 faculties have logged their tea. Ready for your final approval!"

## 2. Balance & Financial Alerts

These are critical to keep the money flowing smoothly.

*   **Low Balance Warning:** Triggered automatically when a faculty's balance drops below a threshold (e.g., ₹50).
    *   *Message:* "⚠️ Your tea fund balance is running low (₹45 remaining). Please top up soon!"
*   **Negative Balance Alert:** Triggered immediately when the Leader approves a day that pushes a faculty into the negative.
    *   *Message:* "🚨 Your tea balance is now negative (-₹15). Please clear your pending payment with the Leader."
*   **Money Added Confirmation:** Triggered when the Leader manually adds money to a faculty's account. This acts as a digital receipt.
    *   *Message:* "💰 ₹500 has been added to your tea fund by the Leader! Current balance: ₹485."

## 3. Administrative Notifications (Leader Only)

*   **New Join Request:** Triggered when someone enters the Secret Code.
    *   *Message:* "👤 John Doe wants to join your Tea Group. Tap to accept or decline."
*   **Missing Data Alert:** If the Leader tries to click "Approve All" but 5 people still haven't logged anything, a popup shows:
    *   *WarningPopup:* "Wait! 5 faculties haven't logged their tea today. Do you want to mark them all as 'Absent' or leave them pending?"

## 4. Notification Settings
*   **Opt-Out:** faculties should be able to silence the "4:00 PM Nudge" if they prefer, but they *cannot* turn off Financial Alerts.
