# Printer Testing – Scenario 2.3: Long Press & Button Hold Behavior

Scenario Focus: **Behavior when physical buttons are pressed and held for extended durations**
This scenario validates how the printer interprets **long-press actions**, avoids accidental triggers, and safely differentiates between short press vs long press.

As requested, this is a **separate file**, and **test cases are numbered from 1 to 10**.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                          | Module / Feature | Test Step No. | Step Description                   | Keyword (Action) | Test Object / Element    | Input Data          | Expected Result                   | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | --------------------------------------- | ---------------- | ------------- | ---------------------------------- | ---------------- | ------------------------ | ------------------- | --------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Device | PR-2.3-TC-01 | Power Button Long Press (Soft Shutdown) | Button Hold      | 1             | Press and hold power button        | Press & Hold     | Power Button             | 5 seconds           | Printer shuts down gracefully     |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Device | PR-2.3-TC-02 | Power Button Extended Hold (Force Off)  | Button Hold      | 1             | Press and hold power button longer | Press & Hold     | Power Button             | 10–15 seconds       | Printer force powers off safely   |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Device | PR-2.3-TC-03 | Cancel Button Long Press                | Button Hold      | 1             | Press and hold Cancel button       | Press & Hold     | Cancel Button            | 5 seconds           | Active job cancelled once         |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Device | PR-2.3-TC-04 | Resume Button Long Press                | Button Hold      | 1             | Press and hold Resume button       | Press & Hold     | Resume Button            | 5 seconds           | No unintended behavior            |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Device | PR-2.3-TC-05 | Wi‑Fi Button Long Press (Setup Mode)    | Button Hold      | 1             | Press and hold Wi‑Fi button        | Press & Hold     | Wi‑Fi Button             | 5–10 seconds        | Wi‑Fi setup/reset mode enabled    |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Device | PR-2.3-TC-06 | Scan Button Long Press                  | Button Hold      | 1             | Press and hold Scan button         | Press & Hold     | Scan Button              | 5 seconds           | No action or defined behavior     |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Device | PR-2.3-TC-07 | Copy Button Long Press                  | Button Hold      | 1             | Press and hold Copy button         | Press & Hold     | Copy Button              | 5 seconds           | Single copy action only           |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Device | PR-2.3-TC-08 | Button Hold During Active Print         | Button Hold      | 1             | Hold any button during print       | Press & Hold     | Any Button               | While printing      | Printer ignores or handles safely |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Device | PR-2.3-TC-09 | Button Hold During Error State          | Button Hold      | 1             | Hold buttons during error          | Press & Hold     | All Buttons              | Error present       | Only valid recovery allowed       |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-2.3-TC-10 | Accidental Button Hold (Pocket Test)    | Button Hold      | 1             | Simulate accidental long press     | Press & Hold     | Power / Function Buttons | Continuous pressure | No unsafe operation               |               |                    |                  |              |

---

### Notes

* Long-press logic is a **common source of firmware bugs**.
* These tests prevent accidental resets, shutdowns, or mode switches.
* Especially important for **consumer devices and safety compliance**.

