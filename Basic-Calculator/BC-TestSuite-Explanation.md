# BASIC CALCULATOR TEST SUITE – DETAILED EXPLANATIONS (PART 1: TESTS 1–25)

Below are the first **25 test suite explanations**, grouped by test type and written in a long, clear, simple, very detailed way. These explanations focus on understanding *why the test exists*, *what it validates*, and *what underlying logic is being exercised*.

---

# **SECTION 1 — BASIC ARITHMETIC OPERATIONS**

These tests verify that the four fundamental calculator operations behave exactly as they should. Although they look simple on the surface, these tests ensure the entire computational engine is behaving reliably.

---

## **TEST 1 — Addition of Two Positive Integers**

**Purpose:** To confirm the calculator performs correct addition when both numbers are positive whole numbers.

**Explanation:** This test ensures that pressing a sequence like `2 + 3 =` actually results in `5`. It might sound trivial, but this verifies the basic operator wiring, the internal state machine that stores the first operand, and the correctness of the add function. If the calculator fails here, nothing else can be trusted.

---

## **TEST 2 — Addition of Two Negative Integers**

**Purpose:** Verify the calculator correctly interprets the minus sign when used as a negative indicator, not an operator.

**Explanation:** When users input `-5 + -3`, the calculator must treat both `-5` and `-3` as valid operands, not mistakenly read them as subtraction. This checks internal parsing rules, sign-handling logic, and whether negative numbers are consistently recognized.

---

## **TEST 3 — Addition with Zero**

**Purpose:** Confirm that adding zero never alters the other value.

**Explanation:** Zero is an identity element in addition. This test ensures the calculator doesn’t apply formatting errors, trailing decimals, or interpret `0` as a null value. It also ensures pressing `0` does not accidentally clear the operand.

---

## **TEST 4 — Subtraction of Two Positive Numbers**

**Purpose:** Validate the accuracy of basic subtraction.

**Explanation:** This test checks that the calculator correctly performs operations like `9 - 4 = 5`. It ensures the operator assignment for subtraction is correctly wired and that the internal logic subtracts the second operand from the first, not the other way around.

---

## **TEST 5 — Subtraction Producing Negative Result**

**Purpose:** Verify output formatting when result is negative.

**Explanation:** A sequence like `4 - 9 = -5` tests whether the calculator can display a negative result cleanly. This includes verifying the position of the minus sign, ensuring no extra spaces, and confirming the result remains selectable for further operations.

---

## **TEST 6 — Multiplication of Positive Integers**

**Purpose:** Validate multiplication logic.

**Explanation:** When executing `7 × 8 = 56`, the calculator must correctly multiply integers. This confirms that the multiplication operator references the correct arithmetic module and doesn’t overflow prematurely or mis-format the output.

---

## **TEST 7 — Multiplication Involving Zero**

**Purpose:** Ensure any number multiplied by zero results in zero.

**Explanation:** This tests whether the calculator respects mathematical identity laws. It also checks that entering zero doesn’t reset the current operand accidentally.

---

## **TEST 8 — Division of Two Positive Integers**

**Purpose:** Confirm division logic is working.

**Explanation:** Simple division like `12 ÷ 4 = 3` validates correct calculation and display. It also ensures dividing by integers doesn’t unintentionally create decimal outputs where they aren't needed.

---

## **TEST 9 — Division Resulting in Decimal Output**

**Purpose:** Validate decimal formatting when division results in non-whole numbers.

**Explanation:** Running `5 ÷ 2 = 2.5` checks decimal rendering, trailing zero handling, and the precision rules. The calculator must not round incorrectly or drop the decimal point.

---

## **TEST 10 — Negative Number Arithmetic (Mixed Signs)**

**Purpose:** Validate handling of mixed-sign operations.

**Explanation:** A test like `10 + -2 = 8` ensures the calculator can differentiate between the operator minus and the unary minus sign before a number.

---

## **TEST 11 — Decimal Addition**

**Purpose:** Ensure decimals are added with correct precision.

**Explanation:** Users often input values like `2.5 + 1.25`. This test is especially important because decimal arithmetic exposes floating-point precision issues. The calculator must either use fixed decimal arithmetic or apply proper rounding for display.

---

## **TEST 12 — Decimal Subtraction**

**Purpose:** Verify subtracting decimal numbers yields an accurate decimal result.

**Explanation:** Performing `3.75 - 1.2` checks whether the calculator subtracts digit-by-digit correctly and maintains the decimal place alignment.

---

## **TEST 13 — Decimal Multiplication**

**Purpose:** Validate that multiplying decimals does not distort the decimal placement.

**Explanation:** Example: `1.2 × 3.5 = 4.2`. This confirms correct decimal shift logic internally.

---

## **TEST 14 — Decimal Division**

**Purpose:** Confirm decimal division precision.

**Explanation:** Dividing decimals (e.g., `7.5 ÷ 2.5 = 3`) tests rounding, precision rules, and whether the app correctly reduces repeating decimals.

---

# **SECTION 2 — OPERATOR PRECEDENCE & PARENTHESES**

These tests ensure the calculator evaluates expressions the way real mathematics requires.

---

## **TEST 15 — Precedence: Multiplication Before Addition**

**Purpose:** Validate that `2 + 3 × 4` yields `14`.

**Explanation:** If the calculator evaluates left-to-right instead of using precedence, the result would incorrectly become `20`. This test confirms correct evaluation order.

---

## **TEST 16 — Precedence: Division Before Addition**

**Purpose:** Verify division comes before addition.

**Explanation:** A test such as `10 + 20 ÷ 5` should yield `14`, not `6`. This ensures the parser prioritizes division correctly.

---

## **TEST 17 — Simple Parentheses Handling**

**Purpose:** Ensure parentheses override precedence.

**Explanation:** `(2 + 3) × 4 = 20` validates that expressions inside parentheses are evaluated first.

---

## **TEST 18 — Nested Parentheses**

**Purpose:** Confirm support for multi-level grouping.

**Explanation:** Expression like `2 × (3 + (4 × 2))` verifies recursion in expression evaluation.

---

## **TEST 19 — Parentheses with Mixed Operators**

**Purpose:** Test prioritization with multiple nested operations.

**Explanation:** Example: `(1 + 2) × (3 + 4)` ensures separate groups evaluate independently then multiply results.

---

## **TEST 20 — Parentheses Around Negative Numbers**

**Purpose:** Confirm negative numbers inside parentheses are parsed correctly.

**Explanation:** `(-2 + 5) × 3` ensures unary minus signs don’t break grouping.

---

## **TEST 21 — Parentheses Containing Decimals**

**Purpose:** Ensure decimal values inside parentheses are handled cleanly.

**Explanation:** `(2.5 + 3.5) × 2 = 12` confirms decimal arithmetic is consistent within grouped expressions.

---

## **TEST 22 — Misplaced Parenthesis Detection**

**Purpose:** Ensure invalid placement of parentheses triggers an error.

**Explanation:** An expression like `2 + )3(` should be rejected. This tests syntax validation, not arithmetic.

---

## **TEST 23 — Missing Closing Parenthesis**

**Purpose:** Detect incomplete expressions.

**Explanation:** `(2 + 3 × 4` should result in either an error or prompt to complete expression. This ensures the parser tracks pairings.

---

## **TEST 24 — Multiple Levels of Precedence**

**Purpose:** Validate complex but valid expressions.

**Explanation:** Expression: `2 + 3 × 4 - 6 ÷ 2` tests mixed operator handling without parentheses.

---

## **TEST 25 — Parentheses with Sequential Operations**

**Purpose:** Ensure chain calculations and parentheses interact properly.

**Explanation:** Example: `(2 + 2) =` then continuing with `× 3 =` should produce `12`, not restart or misinterpret the expression.

---

# END OF PART 1

Part 2 (Tests 26–50) will be prepared in the next container when requested.
