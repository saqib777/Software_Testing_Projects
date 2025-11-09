<div align="center">
  
# Ministry_of_testing

</div>

A comprehensive collection of **manual and functional test cases** designed for practice sites such as [DemoQA](https://demoqa.com/), [TestSheepNZ](https://testsheepnz.github.io/), and others used in the testing community.

This repository is part of a continuous learning initiative to strengthen real-world testing skills by documenting **detailed test scenarios**, **steps**, **expected results**, and **validation techniques** for various web applications.

---

## Repository Structure

| Folder/File             | Description                                                                                                                                                                            |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BookCart/**           | Contains test cases for [BookCart Azure Application](https://bookcart.azurewebsites.net/). Includes detailed registration and login scenarios.                                         |
| **Basic_Calculator.md** | Manual test cases designed for [TestSheepNZ Basic Calculator](https://testsheepnz.github.io/BasicCalculator.html). Covers input validation, arithmetic operations, and error handling. |
| **README.md**           | Repository overview and usage guide.                                                                                                                                                   |

---

## Test Case Format

All test cases follow a consistent, Excel-compatible format used in **Katalon Studio** and similar tools:

| Sl. No. | DATE       | Application | Test Case ID | Test Case Name                           | Module / Feature  | Test Step No. | Step Description              | Keyword (Action) | Test Object / Element | Input Data                                                                                 | Expected Result         | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time |
| ------- | ---------- | ----------- | ------------ | ---------------------------------------- | ----------------- | ------------- | ----------------------------- | ---------------- | --------------------- | ------------------------------------------------------------------------------------------ | ----------------------- | ------------- | ------------------ | ---------------- | ------------ |
| Example | 2025-11-07 | BookCart    | TC_REG_01    | Verify registration page loads correctly | Registration Form | 1             | Navigate to registration page | Open Browser     | URL bar               | [https://bookcart.azurewebsites.net/register](https://bookcart.azurewebsites.net/register) | Form loads successfully | As expected   | Pass               | UI validated     | 5s           |

---

## Objectives

* Strengthen understanding of **manual testing fundamentals**.
* Practice **test design techniques** (boundary value, equivalence partitioning, positive/negative testing).
* Maintain a centralized collection of test cases for **learning and reference**.
* Improve test documentation quality using a structured, professional format.

---

## Contents (so far)

| Application          | Description                                                        | Status      |
| -------------------- | ------------------------------------------------------------------ | ----------- |
| **BookCart**         | Registration and Login test cases for BookCart Azure demo site     | Completed   |
| **Basic Calculator** | Functional and boundary tests for calculator inputs and operations | Completed   |
| **Upcoming**         | Additional Ministry of Testing practice sites and DemoQA modules   | In Progress |

---

## How to Use

1. Browse through the folders to explore test cases for each site.
2. Open `.md` files to view detailed test documentation.
3. Export tables directly to Excel or import them into **Katalon Studio**, **TestLink**, or **Zephyr**.
4. Follow the same format if you wish to add new test cases.

---

## Future Enhancements

* Add bug reports and screenshots for failed scenarios.
* Include test data sheets and parameterized inputs.
* Extend repository to automation testing (Selenium, Playwright, etc.).
* Introduce reusable Excel templates and dashboards.

---

## Contributions

Contributions are welcome if you’d like to:

* Add test cases for new practice sites.
* Improve descriptions or documentation.
* Share your learning notes.

Feel free to fork the repository, open an issue, or submit a pull request.

---

## Author

**Mohammed Saqib**
Focused on learning **Software Testing**, **Test Design**, and **Automation** through hands-on practice and open-source collaboration.
