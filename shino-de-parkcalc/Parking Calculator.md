# ParkCalc Website – Full Testing Documentation  
Comprehensive Test Strategy, Coverage & Notes  

## 1. INTRODUCTION  
This document covers testing of the ParkCalc web application, which allows users to calculate parking cost based on parking lot type, entry/exit times and dates. The tool is publicly accessible and frequently used for testing exercises. :contentReference[oaicite:1]{index=1}  
Ensuring accuracy, reliability, usability and robustness is crucial since users rely on correct cost estimates.

## 2. SCOPE OF TESTING  
### Included in Scope  
- Selection of parking lot type (Valet, Short-Term, Economy, Long-Term Garage, Long-Term Surface)  
- Entry date/time and exit date/time fields (AM/PM)  
- Cost calculation and correct display of cost and duration  
- Validations for date/time logic (entry <= exit, correct formats)  
- Rate rules: per lot, daily maximums, weekly maximums (some free day rules) :contentReference[oaicite:2]{index=2}  
- UI elements: dropdowns, date/time pickers, buttons, result display  
- Error messages for invalid inputs (wrong date formats, exit before entry, too long duration)  
- Responsiveness, browser compatibility, accessibility (basic)  
- Performance under varied durations and edge-cases (very long durations, boundaries)  

### Out of Scope  
- Backend database calculation algorithms (black-box view)  
- Authentication/ login flows (not part of public calculator)  
- Paid user account behaviours or APIs  
- Non-public features of the system  

## 3. TESTING OBJECTIVES  
- Confirm the cost calculation follows the published rate tables.  
- Ensure correct duration is computed (days, hours, minutes).  
- Validate form input and error handling for invalid data.  
- Verify UI clarity, usability and alignment of form elements.  
- Assess behaviour in edge and negative scenarios (very long durations, bogus times).  
- Check accessibility and responsiveness across devices.  
- Identify defects in business rules implementation (rates, max days, etc.).  

## 4. MODULES COVERED  
### 4.1 Lot Type Selection  
Verifies that all lot types are available, selectable, and correspond to their rate rules.  
### 4.2 Entry & Exit Date/Time Inputs  
Tests the date/time fields for correct input handling, AM/PM options and validation.  
### 4.3 Cost and Duration Display  
Validates correct cost output and formatted display of “X Days, Y Hours, Z Minutes”.  
### 4.4 Validation & Error Handling  
Covers invalid formats, entry date after exit date, durations beyond allowed maximums, missing inputs.  
### 4.5 UI / Responsiveness  
Form layout across desktop, tablet and mobile; visibility of result area; accessibility check.  
### 4.6 Edge & Performance Cases  
Very short durations (minutes), very long durations (weeks), large numbers; performance under repeated uses.  
### 4.7 Compatibility & Browser Behaviour  
Runs across major browsers (Chrome, Firefox, Edge, Safari) with consistent results.  

## 5. TESTING TYPES APPLIED  
### 5.1 Functional Testing  
Selecting lot type → entering dates/times → clicking “Calculate” → verifying correct output.  
### 5.2 Input & Validation Testing  
Invalid inputs, missing data, incorrect formats, logical errors (exit < entry).  
### 5.3 UI/UX Testing  
Form element visibility, layout, readability, date/time pickers.  
### 5.4 Accessibility Testing  
Keyboard navigation, labels, correct usage of fields, result readability.  
### 5.5 Performance & Boundary Testing  
Very short/long durations, stress testing of calculation logic.  
### 5.6 Compatibility Testing  
Different browsers/devices, date/time formatting variations.  
### 5.7 Negative & Security Testing  
Try to generate extreme values, durations outside rules, malformed input.  

## 6. ASSUMPTIONS  
- The site is publicly accessible and usable.  
- Rates shown are current and correctly configured as per published table.  
- Time zones are consistent (application uses local time).  
- Date/time pickers operate per expected format (MM/DD/YYYY or similar).  

## 7. RISKS  
- Mis-interpretation of published rate rules may lead to wrong expected results.  
- Date/time logic may vary by browser locale settings.  
- Extremely large durations may cause overflow or formatting issues.  
- Third-party UI components (date-picker) may behave differently in older browsers.  

## 8. ENTRY CRITERIA  
- Application is live and accessible.  
- Rate table is confirmed.  
- Test data (dates, times) defined.  
- Browsers & test environment set up.  

## 9. EXIT CRITERIA  
- All planned test cases executed.  
- No high/critical defects remain.  
- Results documented and signed off.  
- Regression for any fixes executed.  

## 10. DEFECT REPORTING PROCESS  
When raising a defect include:  
- Environment (browser, OS)  
- Lot type selected  
- Entry/exit date & time  
- Expected cost & result  
- Actual result visible  
- Screenshot or record of duration & cost display  

## 11. NOTES & BEST PRACTICES  
- Always test minimal and maximal durations.  
- Validate also intermediate rule points (e.g., daily maximum, weekly maximum).  
- Check AM/PM switches carefully.  
- Use consistent format when comparing expected vs actual.  
- Keep track of locale/time format issues (e.g., MM/DD vs DD/MM).  
- Capture any strange behaviour for durations > 7 days (some documentation says “7th day free” for long-term lots).  

## 12. SUMMARY  
This document lays out a robust plan for testing the ParkCalc application.  
It covers business logic, UI, boundary conditions, negative tests and usability factors.  

| Sl. No. | DATE       | Application  | Test Case ID        | Test Case Name                                  | Module/Feature           | Step No. | Step Description                                   | Keyword  | Test Object/Element           | Input Data                                  | Expected Result                                      | Actual Result | Status | Comments/Notes                                   | Time |
|---------|------------|--------------|----------------------|--------------------------------------------------|---------------------------|----------|---------------------------------------------------|----------|------------------------------|---------------------------------------------|-----------------------------------------------------|---------------|--------|--------------------------------------------------|------|
| 1       | 2025-11-19 | ParkCalc     | TC_PC_01             | Short-Term Parking – 1 hour                      | Functional                 | 1        | Select “Short-Term Parking”, enter entry & exit with 1 hour duration | Select/Type | Lot Dropdown, Date/Time Fields   | Lot=Short-Term, Entry=09/15/2025 10:00 AM, Exit=09/15/2025 11:00 AM | Cost = $2.00 (first hour)                              |               |        | Validates base rate                                   |      |
| 2       | 2025-11-19 | ParkCalc     | TC_PC_02             | Short-Term Parking – 2.5 hours                   | Functional                 | 1        | Select Lot, entry & exit with 2h30m             | Select/Type | Fields                        | Lot=Short-Term, Entry=10/01/2025 14:00 PM, Exit=10/01/2025 16:30 PM | Cost = $2.00 + $1 for each half-hour after first (Total $5.00) |               |        | Check incremental half-hour charge                     |      |
| 3       | 2025-11-19 | ParkCalc     | TC_PC_03             | Short-Term Parking – daily maximum               | Boundary                   | 1        | Span >24 hours but within daily max              | Select/Type | Fields                        | Lot=Short-Term, Entry=07/01/2025 08:00 AM, Exit=07/02/2025 09:00 AM | Cost = $24.00 (daily max)                               |               |        | Validates cap                                         |      |
| 4       | 2025-11-19 | ParkCalc     | TC_PC_04             | Economy Parking – 1 day                          | Functional                 | 1        | Select “Economy Lot”, 24h duration              | Select/Type | Fields                        | Lot=Economy, Entry=08/10/2025 09:00 AM, Exit=08/11/2025 09:00 AM    | Cost = $9.00 (daily max for economy)                   |               |        | Verify economy rates                                |      |
| 5       | 2025-11-19 | ParkCalc     | TC_PC_05             | Long-Term Garage – 1 week (7 days)              | Functional                 | 1        | Lot=Long-Term Garage, duration = 7 days          | Select/Type | Fields                        | Lot=Long-Term Garage, Entry=09/01/2025 12:00 PM, Exit=09/08/2025 12:00 PM | Cost = $72.00 (max week)                                |               |        | Weekly max test                                    |      |
| 6       | 2025-11-19 | ParkCalc     | TC_PC_06             | Valet Parking – ≤ 5 hours                        | Functional                 | 1        | Lot=Valet, duration less than or equal 5 hours   | Select/Type | Fields                        | Lot=Valet, Entry=10/20/2025 08:00 AM, Exit=10/20/2025 13:00 PM     | Cost = $12.00 (for ≤5 hours)                           |               |        | Configure special valet rule                          |      |
| 7       | 2025-11-19 | ParkCalc     | TC_PC_07             | Valet Parking – >5 hours but ≤1 day              | Functional                 | 1        | Lot=Valet, duration >5h but <24h                 | Select/Type | Fields                        | Lot=Valet, Entry=11/05/2025 09:00 AM, Exit=11/05/2025 18:00 PM     | Cost = $18.00 (daily rate)                             |               |        | Validate tiered valet rate                            |      |
| 8       | 2025-11-19 | ParkCalc     | TC_PC_08             | Invalid: Exit before entry                       | Negative                   | 1        | Entry date/time > exit date/time                 | Select/Type | Fields                        | Lot=Economy, Entry=12/10/2025 10:00 AM, Exit=12/10/2025 09:00 AM    | Error message displayed                                 |               | Fail   | Logical validation                                   |      |
| 9       | 2025-11-19 | ParkCalc     | TC_PC_09             | Invalid: Entry date format wrong                 | Negative                   | 1        | Submit with malformed date                        | Select/Type | Fields                        | Lot=Short-Term, Entry=13/32/2025 10:00 AM, Exit=13/33/2025 11:00 AM  | Error message displayed                                 |               | Fail   | Format validation                                   |      |
| 10      | 2025-11-19 | ParkCalc     | TC_PC_10             | Edge Case: Duration zero (same entry and exit)   | Boundary                   | 1        | Entry and exit identical time                    | Select/Type | Fields                        | Lot=Economy, Entry=09/20/2025 10:00 AM, Exit=09/20/2025 10:00 AM    | Cost calculated correctly (maybe $2 first hour)          |               |        | Minimal duration                                     |      |
| 11      | 2025-11-19 | ParkCalc     | TC_PC_11             | Edge Case: Very long duration (>30 days)         | Boundary                   | 1        | Duration beyond typical use                      | Select/Type | Fields                        | Lot=Long-Term Surface, Entry=07/01/2025 12:00 PM, Exit=08/05/2025 12:00 PM | Check for weekly caps or error handling                 |               |        | Overflow duration test                             |      |
| 12      | 2025-11-19 | ParkCalc     | TC_PC_12             | Verify correct time difference display            | Functional                 | 1        | Check the days/hours/min format in result       | Select/Type | Fields                        | Lot=Short-Term, Entry=10/15/2025 08:00 AM, Exit=10/17/2025 10:30 AM  | “2 Days, 2 Hours, 30 Minutes” (or equivalent)            |               |        | Duration display correctness                      |      |
| 13      | 2025-11-19 | ParkCalc     | TC_PC_13             | Verify AM/PM toggle behaviour                     | Functional                 | 1        | Use AM, then PM selections                        | Select/Type | Fields                        | Lot=Economy, Entry=10/05/2025 11:00 PM, Exit=10/06/2025 02:00 AM    | Correct calculation across AM/PM boundary                |               |        | Time of day edge handling                          |      |
| 14      | 2025-11-19 | ParkCalc     | TC_PC_14             | Verify daily maximum enforcement                   | Boundary                   | 1        | Use hours > daily max threshold                  | Select/Type | Fields                        | Lot=Economy, Entry=10/01/2025 00:00 AM, Exit=10/02/2025 12:00 PM    | Cost = daily max (e.g., $9 for economy)                   |               |        | Cap rule validation                                |      |
| 15      | 2025-11-19 | ParkCalc     | TC_PC_15             | Verify weekly maximum enforcement                  | Boundary                   | 1        | Use duration 7 days exactly                        | Select/Type | Fields                        | Lot=Long-Term Garage, Entry=01/01/2025 12:00 PM, Exit=01/08/2025 12:00 PM | Cost = week max ($72 for long-term garage)                |               |        | Weekly cap validation                               |      |
| 16      | 2025-11-19 | ParkCalc     | TC_PC_16             | Invalid: Entry date later than exit date/time     | Negative                   | 1        | Entry date/time > exit                           | Select/Type | Fields                        | Lot=Short-Term, Entry=10/10/2025 10:00 AM, Exit=10/09/2025 09:00 AM    | Error message displayed                                 |               | Fail   | Date logic validation                              |      |
| 17      | 2025-11-19 | ParkCalc     | TC_PC_17             | Changing lot type after entry                      | Functional                 | 1        | Enter info then switch lot and re-run           | Select/Type | Dropdown/Fields               | Lot changed mid-flow            | Correct recalculation perhaps, or prompt to reset        |               |        | Workflow scenario                                     |      |
| 18      | 2025-11-19 | ParkCalc     | TC_PC_18             | Verify lost ticket fee message (if present)       | Functional                 | 1        | Check if lost ticket fee appears for lots        | Inspect    | Result/Message                | –                       | “Lost Ticket Fee: $10.00” included if conditions met      |               |        | Conditional rule check                                |      |
| 19      | 2025-11-19 | ParkCalc     | TC_PC_19             | Verify date picker UI opens correctly              | UI                          | 1        | Click date picker icon for entry/exit             | Click     | Calendar Widget               | –                       | Calendar opens and date selectable                             |               |        | UI widget behaviour                                 |      |
| 20      | 2025-11-19 | ParkCalc     | TC_PC_20             | Mobile view usability test                         | UX/Responsive            | 1        | Open site on mobile resolution                    | Resize    | Browser Window                | –                       | Form elements readable, no overlapping                    |               |        | Mobile UX check                                     |      |

By executing the accompanying test cases, you’ll be able to assure that the calculator provides accurate and reliable results under diverse conditions.

