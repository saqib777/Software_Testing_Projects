# Printer Testing – Scenario 4.2: Wi‑Fi Setup & Network Connectivity

Scenario Focus: **Wireless setup, network stability, and recovery for a Wi‑Fi–enabled printer**
This scenario validates first‑time Wi‑Fi setup, error handling for incorrect credentials, network changes, and stability during use.

This is a **separate file**, and **test cases are numbered from 1 to 10**, consistent with your per‑scenario structure.

---

| Sl. No. | DATE       | Application    | Test Case ID | Test Case Name                   | Module / Feature | Test Step No. | Step Description                        | Keyword (Action) | Test Object / Element | Input Data              | Expected Result                         | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | -------------- | ------------ | -------------------------------- | ---------------- | ------------- | --------------------------------------- | ---------------- | --------------------- | ----------------------- | --------------------------------------- | ------------- | ------------------ | ---------------- | ------------ |
| 1       | 2025-11-28 | Printer Device | PR-4.2-TC-01 | Enter Correct Wi‑Fi Credentials  | Wi‑Fi Setup      | 1             | Start Wi‑Fi setup and enter credentials | Input            | Wi‑Fi Setup Screen    | SSID + correct password | Printer connects successfully           |               |                    |                  |              |
| 2       | 2025-11-28 | Printer Device | PR-4.2-TC-02 | Enter Incorrect Wi‑Fi Password   | Wi‑Fi Setup      | 1             | Enter wrong Wi‑Fi password              | Input            | Wi‑Fi Setup Screen    | Wrong password          | Clear error shown; retry allowed        |               |                    |                  |              |
| 3       | 2025-11-28 | Printer Device | PR-4.2-TC-03 | Hidden SSID Connection           | Wi‑Fi Setup      | 1             | Attempt to connect to hidden SSID       | Input            | Network List          | Hidden SSID             | Manual entry supported                  |               |                    |                  |              |
| 4       | 2025-11-28 | Printer Device | PR-4.2-TC-04 | Weak Signal During Setup         | Wi‑Fi Setup      | 1             | Start setup with weak signal            | Observe          | Wi‑Fi Antenna         | Low signal              | Warning shown or setup fails gracefully |               |                    |                  |              |
| 5       | 2025-11-28 | Printer Device | PR-4.2-TC-05 | Router Turned Off During Setup   | Wi‑Fi Setup      | 1             | Power off router mid‑setup              | Power Off        | Router                | —                       | Setup fails safely with guidance        |               |                    |                  |              |
| 6       | 2025-11-28 | Printer Device | PR-4.2-TC-06 | Wi‑Fi Disconnect During Printing | Wi‑Fi Stability  | 1             | Disconnect Wi‑Fi during active print    | Disconnect       | Network               | During print            | Print pauses or errors safely           |               |                    |                  |              |
| 7       | 2025-11-28 | Printer Device | PR-4.2-TC-07 | Network Change After Setup       | Wi‑Fi Setup      | 1             | Change router/network name              | Change           | Router                | New SSID                | Printer prompts for re‑setup            |               |                    |                  |              |
| 8       | 2025-11-28 | Printer Device | PR-4.2-TC-08 | Reconnect to Wi‑Fi After Restart | Wi‑Fi Stability  | 1             | Restart printer                         | Restart          | Power Button          | —                       | Auto‑reconnects to saved network        |               |                    |                  |              |
| 9       | 2025-11-28 | Printer Device | PR-4.2-TC-09 | Multiple Devices on Same Wi‑Fi   | Wi‑Fi Usage      | 1             | Send print jobs from two devices        | Print            | Network Queue         | Two devices             | Jobs queued and handled correctly       |               |                    |                  |              |
| 10      | 2025-11-28 | Printer Device | PR-4.2-TC-10 | Wi‑Fi Signal Drop & Recovery     | Wi‑Fi Stability  | 1             | Temporarily drop Wi‑Fi signal           | Simulate         | Network               | Signal loss             | Printer recovers when signal returns    |               |                    |                  |              |

---

### Notes

* Wi‑Fi issues are the **most common consumer complaints** for printers.
* These tests validate **setup clarity**, **error messaging**, and **automatic recovery**.
* Strong coverage here reduces support tickets significantly.

