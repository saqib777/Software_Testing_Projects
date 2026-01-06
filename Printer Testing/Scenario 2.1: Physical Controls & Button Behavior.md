# Printer Testing - Scenario 2.1: Physical Controls & Button Behavior

Scenario Focus: **Behavior of physical buttons during normal conditions**

These test cases validate how the printer responds when users interact with **physical buttons** such as Power, Cancel, Resume, Scan, Copy, and Wi‑Fi.
All test cases are written in your **standard table format** and are meant to be appended after Scenario 1.2.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                   | Module / Feature | Test Step No. | Step Description                           | Keyword (Action) | Test Object / Element | Input Data       | Expected Result                     | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | -------------------------------- | ---------------- | ------------- | ------------------------------------------ | ---------------- | --------------------- | ---------------- | ----------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 01      | 2025-11-28 | Printer Device | PR-TC-11     | Power Button Single Press        | Button Behavior  | 1             | Press Power button once when printer is ON | Press            | Power Button          | —                | Printer initiates shutdown sequence |               |                    |                  |              |
| 02      | 2025-11-28 | Printer Device | PR-TC-12     | Power Button Press When OFF      | Button Behavior  | 1             | Press Power button when printer is OFF     | Press            | Power Button          | —                | Printer powers ON successfully      |               |                    |                  |              |
| 03      | 2025-11-28 | Printer Device | PR-TC-13     | Cancel Button Without Active Job | Button Behavior  | 1             | Press Cancel button with no job            | Press            | Cancel Button         | —                | No action or gentle notification    |               |                    |                  |              |
| 04      | 2025-11-28 | Printer Device | PR-TC-14     | Cancel Button During Print       | Button Behavior  | 1             | Start a print job and press Cancel         | Press            | Cancel Button         | Active print job | Print job stops immediately         |               |                    |                  |              |
| 05      | 2025-11-28 | Printer Device | PR-TC-15     | Resume Button Without Error      | Button Behavior  | 1             | Press Resume when no error exists          | Press            | Resume Button         | —                | No action taken                     |               |                    |                  |              |
| 06      | 2025-11-28 | Printer Device | PR-TC-16     | Resume Button After Error        | Button Behavior  | 1             | Trigger error and press Resume             | Press            | Resume Button         | Paper loaded     | Printer resumes operation           |               |                    |                  |              |
| 07      | 2025-11-28 | Printer Device | PR-TC-17     | Scan Button Without PC Connected | Button Behavior  | 1             | Press Scan button without PC               | Press            | Scan Button           | —                | Error or instruction displayed      |               |                    |                  |              |
| 08      | 2025-11-28 | Printer Device | PR-TC-18     | Copy Button Single Press         | Button Behavior  | 1             | Press Copy button once                     | Press            | Copy Button           | —                | Printer starts copy process         |               |                    |                  |              |
| 09      | 2025-11-28 | Printer Device | PR-TC-19     | Wi‑Fi Button Single Press        | Button Behavior  | 1             | Press Wi‑Fi button once                    | Press            | Wi‑Fi Button          | —                | Wi‑Fi setup/status mode activated   |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-TC-20     | Button Response Time             | Button Behavior  | 1             | Press any button and observe delay         | Observe          | All Buttons           | —                | Response within acceptable time     |               |                    |                  |              |

---

### Notes

* These test cases assume **normal operating conditions** (no power loss, no hardware fault).
* They validate **predictability**, **user feedback**, and **safe handling** of button actions.
* Many real-world defects are caused by poor button-state handling.

