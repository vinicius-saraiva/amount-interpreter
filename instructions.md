💡 Page Functional Specs
1️⃣ Features
✅ Single input field to type or paste an amount.
✅ Automatic formatting when the user types or pastes.
✅ Thousand separator detection & normalization.
✅ Decimal separator correction (e.g., 1.234,56 → 1234.56).
✅ Space handling (1 234,56 → 1234.56).
✅ Ignore currency symbols and codes ($1,234.56 → 1234.56).
✅ Live preview of the parsed number.

2️⃣ Parsing Rules
1️⃣ Trim whitespace.
2️⃣ Remove currency symbols and codes (€, $, USD, etc.).
3️⃣ Detect separators:

If both , and . exist → Use the last occurrence to determine the decimal separator.
If only , exists → Assume it's a decimal separator.
If only . exists → Assume it's a decimal separator.
4️⃣ Remove thousands separators.
5️⃣ Convert the decimal separator to ..
6️⃣ Convert the string to a float.

3️⃣ Edge Cases Handled
✅ Comma vs. dot conflicts (1,234.56 vs. 1.234,56).
✅ Users typing spaces manually (1 234,56).
✅ Large numbers with separators (123.456.789,00).
✅ Raw numbers without separators (123456.78).
✅ Invalid input handling (letters, mixed symbols).

📜 HTML & JavaScript Implementation
Here's the full code for a webpage that implements these specs:

🔹 Features
Uses vanilla JavaScript (no libraries needed).
Provides real-time feedback on parsed amounts.
Allows both pasting & typing while handling different formats.

Handles different formats (1.234,56, 123,456.78, etc.).
Removes currency symbols (€, $, USD).
Standardizes numbers to 123456.78 format.
Works while typing or pasting.
Try it out! Let me know if you need tweaks. 😊