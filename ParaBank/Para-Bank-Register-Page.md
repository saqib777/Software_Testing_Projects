# ParaBank Registration Testing

This document contains detailed manual test cases for the **ParaBank Registration Page**  
URL: [https://parabank.parasoft.com/parabank/register.htm](https://parabank.parasoft.com/parabank/register.htm)

The objective of this test suite is to validate all user registration functionalities, field-level validations, and system responses under different scenarios, both positive and negative.

---

## Test Case Table

| Sl. No. | DATE | Application | Test Case ID | Test Case Name | Module / Feature | Test Step No. | Step Description | Keyword (Action) | Test Object / Element | Input Data | Expected Result | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed Time |
|----------|------|--------------|---------------|----------------|------------------|----------------|------------------|------------------|------------------------|-------------|-----------------|----------------|--------------------|------------------|---------------|
| 1 | 12-Nov-2025 | ParaBank | TC_REG_001 | Verify registration page loads | Registration | 1 | Navigate to the ParaBank registration URL | Open URL | Registration page | N/A | Page loads successfully with all fields visible | | | Page should load within 3 seconds | 00:10 |
| 2 | 12-Nov-2025 | ParaBank | TC_REG_002 | Verify “First Name” field presence | Registration | 1 | Check if First Name input box is present | Visual Check | First Name input | N/A | Field visible and accepts input | | | Should not overlap with other elements | 00:06 |
| 3 | 12-Nov-2025 | ParaBank | TC_REG_003 | Verify “Last Name” field presence | Registration | 1 | Check if Last Name input box is visible | Visual Check | Last Name input | N/A | Field visible and accepts text input | | | Aligned properly with label | 00:05 |
| 4 | 12-Nov-2025 | ParaBank | TC_REG_004 | Verify “Address” field | Registration | 1 | Validate address field accepts characters and numbers | Enter Text | Address input | “123 Elm Street” | Field accepts input correctly | | | Supports alphanumeric input | 00:08 |
| 5 | 12-Nov-2025 | ParaBank | TC_REG_005 | Verify “City” field | Registration | 1 | Check City field functionality | Enter Text | City input | “Los Angeles” | Field accepts valid input | | | Should reject numbers | 00:08 |
| 6 | 12-Nov-2025 | ParaBank | TC_REG_006 | Verify “State” field | Registration | 1 | Check State field input | Enter Text | State input | “California” | Field accepts text input | | | Alphabetic only | 00:07 |
| 7 | 12-Nov-2025 | ParaBank | TC_REG_007 | Verify “Zip Code” accepts only numbers | Registration | 1 | Enter alphabets in Zip Code field | Enter Text | Zip Code input | “ABCDE” | Error message displayed | | | Validation message shown | 00:09 |
| 8 | 12-Nov-2025 | ParaBank | TC_REG_008 | Verify “Phone #” field format | Registration | 1 | Enter text in Phone number field | Enter Text | Phone # input | “abcde123” | Error or format restriction | | | Should allow only digits | 00:09 |
| 9 | 12-Nov-2025 | ParaBank | TC_REG_009 | Verify SSN field accepts digits only | Registration | 1 | Enter invalid SSN format | Enter Text | SSN input | “abc123” | Error message displayed | | | SSN must be numeric | 00:08 |
| 10 | 12-Nov-2025 | ParaBank | TC_REG_010 | Verify “Username” field presence | Registration | 1 | Check if username field is visible | Visual Check | Username input | N/A | Field visible | | | Unique input expected | 00:06 |
| 11 | 12-Nov-2025 | ParaBank | TC_REG_011 | Verify password masking | Registration | 1 | Enter text in password field | Enter Text | Password input | “Secret123” | Characters hidden as ••••• | | | Masking confirmed | 00:07 |
| 12 | 12-Nov-2025 | ParaBank | TC_REG_012 | Verify confirm password match validation | Registration | 1 | Enter mismatched passwords | Enter Text / Click | Password + Confirm | “12345” / “54321” | Error “Passwords do not match” | | | Proper validation required | 00:10 |
| 13 | 12-Nov-2025 | ParaBank | TC_REG_013 | Validate empty form submission | Registration | 1 | Leave all fields blank and click register | Click Button | Register button | Empty | Error displayed for required fields | | | Prevents form submission | 00:09 |
| 14 | 12-Nov-2025 | ParaBank | TC_REG_014 | Verify successful registration with valid data | Registration | 1 | Fill all fields correctly | Enter Text / Click | All input fields | Valid test data | Registration success message shown | | | Confirmation displayed | 00:15 |
| 15 | 12-Nov-2025 | ParaBank | TC_REG_015 | Verify duplicate username validation | Registration | 1 | Register with existing username | Enter Text / Click | Username field | “ExistingUser” | Error “Username already exists” | | | Validation enforced | 00:12 |
| 16 | 12-Nov-2025 | ParaBank | TC_REG_016 | Verify field length constraints | Registration | 1 | Enter 300 characters in address | Enter Text | Address field | Long text | Error or field truncates | | | Input limit validated | 00:11 |
| 17 | 12-Nov-2025 | ParaBank | TC_REG_017 | Verify form reset functionality | Registration | 1 | Enter data then reload page | Refresh | Registration form | N/A | Form cleared | | | Page refresh clears data | 00:07 |
| 18 | 12-Nov-2025 | ParaBank | TC_REG_018 | Verify all field labels visible | UI Validation | 1 | Check if all input labels visible | Visual Check | All labels | N/A | Labels match field names | | | UI clarity ensured | 00:06 |
| 19 | 12-Nov-2025 | ParaBank | TC_REG_019 | Verify keyboard navigation (tab order) | Accessibility | 1 | Press Tab key through all fields | Press Tab | Input fields | N/A | Focus moves in logical order | | | Accessibility verified | 00:09 |
| 20 | 12-Nov-2025 | ParaBank | TC_REG_020 | Verify form alignment and spacing | UI Validation | 1 | Inspect field spacing | Visual Check | Registration form | N/A | Properly aligned fields | | | Clean layout | 00:06 |
| 21 | 12-Nov-2025 | ParaBank | TC_REG_021 | Verify error messages are styled correctly | UI Validation | 1 | Trigger validation error | Enter Invalid Data | Any input field | Invalid entry | Error message appears in red | | | Color contrast adequate | 00:07 |
| 22 | 12-Nov-2025 | ParaBank | TC_REG_022 | Verify password minimum length validation | Registration | 1 | Enter short password | Enter Text / Click | Password input | “123” | Error message displayed | | | Minimum length enforced | 00:09 |
| 23 | 12-Nov-2025 | ParaBank | TC_REG_023 | Verify numeric fields restrict characters | Registration | 1 | Enter text in zip code or phone field | Enter Text | Numeric inputs | “ABCDE” | Input rejected | | | JS or backend validation | 00:10 |
| 24 | 12-Nov-2025 | ParaBank | TC_REG_024 | Verify responsiveness on mobile | Responsive UI | 1 | Resize browser window | Resize Browser | Registration page | – | Page responsive and scrollable | | | Works across devices | 00:14 |
| 25 | 12-Nov-2025 | ParaBank | TC_REG_025 | Verify page title correctness | UI Validation | 1 | Check browser title | Verify Title | Title Bar | – | “ParaBank | Register for Free Online Banking” | | | Consistent branding | 00:05 |
| 26 | 12-Nov-2025 | ParaBank | TC_REG_026 | Verify registration time performance | Performance | 1 | Submit form and measure response time | Click | Register button | Valid data | Form submits in <3 seconds | | | Backend response validated | 00:12 |
| 27 | 12-Nov-2025 | ParaBank | TC_REG_027 | Verify registration after network delay | Network Simulation | 1 | Submit form after throttling network | Delay / Click | Register button | Valid data | Form handles latency gracefully | | | No timeout | 00:18 |
| 28 | 12-Nov-2025 | ParaBank | TC_REG_028 | Verify “Register” button enabled only when valid | Registration | 1 | Leave fields incomplete | Visual Check | Register button | Invalid inputs | Button disabled | | | Prevents accidental submission | 00:08 |
| 29 | 12-Nov-2025 | ParaBank | TC_REG_029 | Verify session timeout handling | Security | 1 | Idle for 10 mins and submit | Wait / Click | Register button | Valid data | Error “Session expired” or re-login | | | Secure session handling | 00:20 |
| 30 | 12-Nov-2025 | ParaBank | TC_REG_030 | Verify registration confirmation message | Registration | 1 | Complete registration | Click | Register button | Valid data | Confirmation message displayed | | | Proper success message | 00:10 |

---

## Notes & Observations

1. **Positive Findings**
   - Registration form fields are clearly labeled and accessible.
   - Input validation works correctly for most numeric fields.
   - Registration flow is intuitive and well-structured.

2. **Issues Observed**
   - Error messages sometimes overlap when multiple fields are invalid.
   - Password mismatch error could be more descriptive.
   - No CAPTCHA or spam prevention present.

3. **Performance Notes**
   - Page load time is within acceptable range.
   - Submission response time averages under 2.5 seconds.
   - Some lag observed under simulated low bandwidth.

4. **Security Observations**
   - Passwords are masked correctly.
   - SSN field should be encrypted during transmission.
   - No rate limiting on registration requests.

---

## Documentation Summary

**Application:** ParaBank  
**Module:** Registration  
**Feature Type:** Functional + UI + Validation  
**Total Test Cases:** 30  
**Tester:** Mohammed Saqib  
**Execution Date:** 12-Nov-2025  
**Tools Used:** Chrome v119, Manual Testing, Excel Template  
**Status:** Completed  

---

## Conclusion

This suite covers full validation of the ParaBank Registration module.  
It ensures that the form supports correct user input, prevents invalid registration, and handles usability and security aspects effectively.  

All test cases conform to the standardized structure used in this repository, ensuring consistency, readability, and easy tracking in Excel or any test management tool.
