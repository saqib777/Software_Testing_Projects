# Printer Testing – Scenario 4.1: USB Connectivity Behavior

Scenario Focus: **Printer behavior when connected via USB cable under normal, incorrect, and changing conditions**
This scenario validates detection, stability, and recovery when using a **USB connection** between printer and computer.

This is a **separate file**, and **test cases are numbered from 1 to 10**, consistent with your project structure.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                     | Module / Feature | Test Step No. | Step Description                              | Keyword (Action) | Test Object / Element | Input Data     | Expected Result                    | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | ---------------------------------- | ---------------- | ------------- | --------------------------------------------- | ---------------- | --------------------- | -------------- | ---------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Device | PR-4.1-TC-01 | USB Connect After Power On         | USB Connectivity | 1             | Connect USB cable after printer is powered ON | Connect          | USB Cable             | Printer ON     | OS detects printer successfully    |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Device | PR-4.1-TC-02 | USB Connect Before Power On        | USB Connectivity | 1             | Connect USB cable before powering printer     | Connect          | USB Cable             | Printer OFF    | Printer detected after power ON    |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Device | PR-4.1-TC-03 | USB Disconnect While Idle          | USB Connectivity | 1             | Disconnect USB cable when idle                | Disconnect       | USB Cable             | Printer idle   | OS updates device status safely    |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Device | PR-4.1-TC-04 | USB Disconnect During Printing     | USB Connectivity | 1             | Unplug USB cable during print job             | Disconnect       | USB Cable             | Active print   | Print stops and error shown        |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Device | PR-4.1-TC-05 | Reconnect USB After Disconnect     | USB Connectivity | 1             | Reconnect USB cable after disconnect          | Reconnect        | USB Cable             | —              | Printer reconnects without restart |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Device | PR-4.1-TC-06 | Use Faulty USB Cable               | USB Connectivity | 1             | Connect using faulty USB cable                | Connect          | USB Cable             | Faulty cable   | Error shown or device not detected |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Device | PR-4.1-TC-07 | Switch USB Ports                   | USB Connectivity | 1             | Change USB port on PC                         | Connect          | USB Port              | Different port | Printer re-detected correctly      |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Device | PR-4.1-TC-08 | USB Hub Connection                 | USB Connectivity | 1             | Connect printer via USB hub                   | Connect          | USB Hub               | Hub connected  | Printer detected and usable        |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Device | PR-4.1-TC-09 | USB Sleep/Wake Behavior            | USB Connectivity | 1             | Put PC to sleep and wake                      | Sleep/Wake       | Operating System      | —              | Printer reconnects automatically   |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-4.1-TC-10 | USB Connection Stability Over Time | USB Connectivity | 1             | Keep USB connected for long duration          | Observe          | USB Connection        | 2+ hours       | No disconnection or errors         |               |                    |                  |              |

---

### Notes

* USB issues are among the **most common printer support problems**.
* These tests validate **stability, recovery, and user feedback**.
* This scenario builds directly on driver installation scenarios.

