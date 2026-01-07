# Printer Testing – Scenario 3.2: Incorrect Driver Installation Order

Scenario Focus: **User installs or connects the printer in the wrong order**
This scenario validates how well the system handles **common user mistakes** during driver installation and whether it guides the user back to a correct state.

This is a **separate file**, and **test cases are numbered from 1 to 10**, consistent with your project structure.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                                      | Module / Feature          | Test Step No. | Step Description                               | Keyword (Action) | Test Object / Element | Input Data          | Expected Result                   | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | --------------------------------------------------- | ------------------------- | ------------- | ---------------------------------------------- | ---------------- | --------------------- | ------------------- | --------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Driver | PR-3.2-TC-01 | Connect Printer Before Driver Install               | Driver Install (Negative) | 1             | Connect printer to PC before installing driver | Connect          | USB Cable             | Printer powered ON  | OS prompts for driver or guidance |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Driver | PR-3.2-TC-02 | OS Auto-Detect Without Driver                       | Driver Install (Negative) | 1             | Allow OS to auto-detect printer                | Detect           | Operating System      | No driver installed | OS shows limited/unknown device   |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Driver | PR-3.2-TC-03 | Start Driver Install With Printer Already Connected | Driver Install (Negative) | 1             | Launch installer with printer connected        | Launch           | Installer             | Printer connected   | Installer handles state correctly |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Driver | PR-3.2-TC-04 | Disconnect Printer During Installation              | Driver Install (Negative) | 1             | Unplug printer mid-installation                | Disconnect       | USB Cable             | During install      | Installer shows clear error       |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Driver | PR-3.2-TC-05 | Cancel Driver Installation Midway                   | Driver Install (Negative) | 1             | Cancel installation before completion          | Cancel           | Installer             | Mid-progress        | Installation rolls back safely    |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Driver | PR-3.2-TC-06 | Re-run Installer After Cancellation                 | Driver Install (Recovery) | 1             | Relaunch installer after cancel                | Relaunch         | Installer             | —                   | Installer resumes cleanly         |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Driver | PR-3.2-TC-07 | Install Wrong OS Driver                             | Driver Install (Negative) | 1             | Attempt to install incompatible driver         | Install          | Installer             | Wrong OS version    | Installation blocked with message |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Driver | PR-3.2-TC-08 | Multiple Installation Attempts                      | Driver Install (Stress)   | 1             | Run installer multiple times                   | Launch           | Installer             | Repeated launches   | No duplicate/conflict created     |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Driver | PR-3.2-TC-09 | Driver Install Without Admin Rights                 | Driver Install (Negative) | 1             | Run installer without admin rights             | Launch           | Installer             | Standard user       | Permission error shown clearly    |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Driver | PR-3.2-TC-10 | Recover After Incorrect Install Order               | Driver Install (Recovery) | 1             | Follow guidance to fix install                 | Recover          | Installer / OS        | Correct steps       | Printer installs successfully     |               |                    |                  |              |

---

### Notes

* These scenarios represent **real user mistakes**, not edge fantasies.
* Good products **guide users back**, not just fail.
* This set pairs perfectly with Scenario 3.1 (Happy Path).

