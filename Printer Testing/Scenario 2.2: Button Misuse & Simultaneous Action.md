# Printer Testing – Scenario 2.2: Button Misuse & Simultaneous Actions

Scenario Focus: **User misuse, stress interaction, and simultaneous button operations**
This scenario validates how the printer behaves when users press buttons in unusual, incorrect, or overlapping ways.

As requested, **test cases are numbered from 1 to 10**, since this is a **separate file per scenario**.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                    | Module / Feature    | Test Step No. | Step Description                            | Keyword (Action) | Test Object / Element  | Input Data       | Expected Result                        | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | --------------------------------- | ------------------- | ------------- | ------------------------------------------- | ---------------- | ---------------------- | ---------------- | -------------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Device | PR-2.2-TC-01 | Rapid Power Button Press          | Button Misuse       | 1             | Press power button rapidly multiple times   | Press            | Power Button           | Rapid presses    | Printer handles input safely, no crash |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Device | PR-2.2-TC-02 | Power Button Press During Startup | Button Misuse       | 1             | Press power button while printer is booting | Press            | Power Button           | During startup   | Printer ignores or shuts down safely   |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Device | PR-2.2-TC-03 | Cancel Button Spam During Print   | Button Misuse       | 1             | Press Cancel repeatedly during active print | Press            | Cancel Button          | Repeated presses | Print stops once without error         |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Device | PR-2.2-TC-04 | Resume Button Spam Without Error  | Button Misuse       | 1             | Press Resume repeatedly with no error       | Press            | Resume Button          | Repeated presses | No unexpected behavior                 |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Device | PR-2.2-TC-05 | Power + Cancel Simultaneous Press | Simultaneous Action | 1             | Press Power and Cancel together             | Press            | Power + Cancel Buttons | Simultaneous     | Printer handles combo safely           |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Device | PR-2.2-TC-06 | Scan + Copy Button Together       | Simultaneous Action | 1             | Press Scan and Copy at same time            | Press            | Scan + Copy Buttons    | Simultaneous     | One action executed or error shown     |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Device | PR-2.2-TC-07 | Wi-Fi Button During Printing      | Simultaneous Action | 1             | Press Wi-Fi button during print job         | Press            | Wi-Fi Button           | While printing   | Print continues or safe pause          |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Device | PR-2.2-TC-08 | Lid Open + Button Press           | Button Misuse       | 1             | Open lid and press any function button      | Press            | Function Buttons       | Lid open         | Warning shown, no operation            |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Device | PR-2.2-TC-09 | Button Press During Error State   | Button Misuse       | 1             | Trigger error and press random buttons      | Press            | All Buttons            | Error active     | Only valid actions allowed             |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-2.2-TC-10 | All Buttons Pressed Sequentially  | Stress              | 1             | Press all buttons one after another quickly | Press            | All Buttons            | Sequential       | No freeze or reboot                    |               |                    |                  |              |

---

### Notes

* These test cases represent **real-world chaotic user behavior**.
* They are critical for **firmware stability and safety certification**.
* Many hardware bugs are exposed only under misuse conditions.


Tell me which one to continue, and I’ll create the next file in the same clean structure.
