# Printer Testing – Scenario 1.2: First Power On

Scenario Focus: **First-time power-on behavior after unboxing**

Below are test cases created **only for Scenario 1.2**, written in your **exact table format** and ready to be appended to a larger printer test suite.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                 | Module / Feature | Test Step No. | Step Description                 | Keyword (Action) | Test Object / Element | Input Data    | Expected Result                 | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | ------------------------------ | ---------------- | ------------- | -------------------------------- | ---------------- | --------------------- | ------------- | ------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Device | PR-TC-01     | Power On with Proper Setup     | First Power On   | 1             | Press power button once          | Press            | Power Button          | —             | Printer powers on successfully  |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Device | PR-TC-02     | Power Indicator Light Status   | First Power On   | 1             | Observe power LED after power on | Observe          | Power LED             | —             | LED turns solid green/blue      |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Device | PR-TC-03     | Startup Sound Behavior         | First Power On   | 1             | Listen during startup            | Observe          | Printer Speaker       | —             | Normal startup sound heard      |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Device | PR-TC-04     | Display Welcome Message        | First Power On   | 1             | Observe display screen           | Verify           | Display Panel         | —             | Welcome/setup message shown     |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Device | PR-TC-05     | Power Button Long Press        | First Power On   | 1             | Press and hold power button      | Press & Hold     | Power Button          | 5 seconds     | Printer powers off or ignores   |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Device | PR-TC-06     | Multiple Power Button Presses  | First Power On   | 1             | Press power button repeatedly    | Press            | Power Button          | Rapid presses | Printer powers on only once     |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Device | PR-TC-07     | Power On Without Ink Installed | First Power On   | 1             | Power on without ink cartridges  | Power On         | Ink Slot              | No ink        | Error or prompt to install ink  |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Device | PR-TC-08     | Power On Without Paper Loaded  | First Power On   | 1             | Power on with empty paper tray   | Power On         | Paper Tray            | No paper      | Printer powers on with warning  |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Device | PR-TC-09     | Power On with Lid Open         | First Power On   | 1             | Power on while lid is open       | Power On         | Printer Lid           | Lid open      | Warning shown or startup paused |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-TC-10     | Power Cut During Startup       | First Power On   | 1             | Turn off power during startup    | Power Off        | Power Source          | Sudden cut    | Printer handles safely          |               |                    |                  |              |

---

### Notes

* These tests validate **hardware readiness**, **user feedback**, and **safe startup behavior**.
* No printing, scanning, or connectivity is involved yet.
* This scenario alone can catch early manufacturing, firmware, and UX issues.

