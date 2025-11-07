# Basic Calculator Testing – TestSheepNZ

## Page Under Test  
**Basic Calculator – TestSheepNZ**  
URL: [https://testsheepnz.github.io/BasicCalculator.html](https://testsheepnz.github.io/BasicCalculator.html) 

---

## Objective  
To validate the functionality of the basic calculator including arithmetic operations (add, subtract, multiply, divide), string concatenation mode, integer mode toggle, input validation, and UI behaviour.

---

## Test Cases

| TC ID         | Description                                                    | Pre-condition                     | Steps                                                                                      | Expected Result                                                                 |
|---------------|----------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| TC_CALC_01    | Verify page loads and form elements visible                     | Page opened                       | 1. Navigate to the URL. <br>2. Observe first number, second number fields; operation dropdown; “Integers only” toggle; calculate button. | All elements visible and enabled.                                               |
| TC_CALC_02    | Addition of two positive integers                              | Integers only mode ON             | 1. Enter 5 in “First number”. <br>2. Enter 3 in “Second number”. <br>3. Select “Add”. <br>4. Click “Calculate”. | Answer shows 8.                                                                  |
| TC_CALC_03    | Subtraction of two positive integers                           | Integers only mode ON             | Same as above but operation = “Subtract”.                                                 | Answer shows 2.                                                                  |
| TC_CALC_04    | Multiplication of two positive integers                        | Integers only mode ON             | Operation = “Multiply”.                                                                    | Answer shows 15.                                                                 |
| TC_CALC_05    | Division of two positive integers                              | Integers only mode ON             | Operation = “Divide”. Enter first=10, second=2.                                            | Answer shows 5.                                                                  |
| TC_CALC_06    | Division by zero                                               | Integers only mode ON             | Enter first number 10, second number 0, operation = “Divide”.                              | Error or special message (“division by zero”) or UI handled appropriately.     |
| TC_CALC_07    | Toggle “Integers only” OFF and perform decimal results         | Integers only mode OFF            | Enter 10.5 and 2.5, operation = “Divide”.                                                 | Answer shows correct decimal result (e.g., 4.2).                                |
| TC_CALC_08    | Concatenate mode (treat inputs as strings)                      | Integers only toggle is disabled  | Select “Concatenate”. Enter “Hello” in first, “World” in second.                            | Answer shows “HelloWorld”.                                                      |
| TC_CALC_09    | Concatenate mode with numeric strings                           | Integers only toggle disabled     | Operation = “Concatenate”. Enter “123” and “456”.                                          | Answer shows “123456”.                                                         |
| TC_CALC_10    | Input validation for non-numeric input in numeric modes         | Integers only ON, non-Concat mode | Enter “abc” in first number. Click calculate.                                             | Error message or input validation prevents calculation.                          |
| TC_CALC_11    | Toggle state persistence check                                  | Page opened                       | Toggle “Integers only” OFF, select “Subtract”, reload page.                                | Previous toggle state resets or is maintained consistently (decide spec).        |
| TC_CALC_12    | Operation dropdown default value                                | Page opened                       | Observe dropdown value.                                                                   | Default operation is “Add” (or documented default).                              |
| TC_CALC_13    | Negative numbers addition                                       | Integers only OFF/ON              | Enter first = -5, second = -10, operation = “Add”.                                        | Answer shows -15.                                                                |
| TC_CALC_14    | Mixed sign multiplication                                       | Integers only ON                  | Enter first = -4, second = 3, operation = “Multiply”.                                     | Answer shows -12.                                                               |
| TC_CALC_15    | Large numbers support                                            | Integers only ON                  | Enter very large numbers (e.g., 99999999, 88888888), multiply.                              | Correct large result displayed (overflow handled gracefully if any).             |
| TC_CALC_16    | Switch between modes and operations                            | Page opened                       | Change operation multiple times and toggle integers only mode.                             | The UI updates and results correct for each new mode.                            |
| TC_CALC_17    | UI responsiveness on mobile/resized viewport                   | Browser resized/mobile            | Resize window to narrow width, perform a calculation.                                      | UI remains usable; fields visible; result correct.                              |
| TC_CALC_18    | Accessibility – tab navigation and focus                       | Page opened                       | Use Tab to move between fields and operation dropdown, press Enter.                         | Each control receives focus; Enter triggers calculation.                         |
| TC_CALC_19    | Clear or new calculation behaviour                              | Page in any result state          | Perform a calculation, then change input values and recalculate.                           | Result updates; previous value overwritten.                                     |
| TC_CALC_20    | Check concatenation mode ignores “Integers only” toggle         | Toggle integers only ON but select “Concatenate” | Enter “10” and “20”.                                                   | Answer shows “1020”; toggle should be disabled or ignored in concat mode.        |

---

## Notes & Explanations  
- This page offers **basic arithmetic operations** plus a **concatenation mode** where inputs are treated as strings.  
- The “Integers only” toggle limits results to integer outputs when enabled.  
- Input validation is essential — non-numeric input in numeric modes must be handled safely.  
- UI behaviour under mode switching, viewport resizing, keyboard navigation, and large value operations should all be verified.

---

## End Notes  
Though simple in appearance, the Basic Calculator application introduces various functional and non-functional test concerns: numeric vs string mode, error conditions (like division by zero or invalid input), UI responsiveness, mode toggles, and accessibility.  
Covering these scenarios helps ensure reliability, correct handling of edge-cases, and a solid user experience.

**File Name:** `basic_calculator_testing.md`  
**Category:** Web UI – Basic Calculator  
**Purpose:** Manual + Automation test documentation  
