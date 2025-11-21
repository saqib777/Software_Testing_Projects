# PHPTRAVELS Demo Site – Full Test Case Suite

This document contains a complete and detailed manual test‑case suite for **PHPTRAVELS Demo Website** ([https://phptravels.com](https://phptravels.com)), including functional, negative, boundary, usability, performance, and admin‑side scenarios.

All test cases follow the user’s standard table structure (Sl. No., DATE, Application, Test Case ID, Test Case Name, Module / Feature, Test Step No., Step Description, Keyword, Test Object / Element, Input Data, Expected Result, Actual Result, Status, Notes, Elapsed time).

---

## 1. General / UI / Navigation

| Sl. No.                                              | DATE | Application | Test Case ID | Test Case Name   | Module / Feature | Test Step No. | Step Description     | Keyword  | Test Object / Element | Input Data                                       | Expected Result          | Actual Result | Status | Notes | Elapsed time |
| ---------------------------------------------------- | ---- | ----------- | ------------ | ---------------- | ---------------- | ------------- | -------------------- | -------- | --------------------- | ------------------------------------------------ | ------------------------ | ------------- | ------ | ----- | ------------ |
| 1                                                    |      | PHPTRAVELS  | GM-001       | Homepage loads   | General/UI       | 1             | Open site URL        | Open URL | Browser               | [https://phptravels.com](https://phptravels.com) | Homepage loads fully     |               |        |       |              |
| 2                                                    |      | PHPTRAVELS  | GM-002       | Navigation links | General/UI       | 1             | Click each menu item | Click    | Header menu           | Flights/Hotels/Tours/Cars                        | Correct pages open       |               |        |       |              |
| 3                                                    |      | PHPTRAVELS  | GM-003       | Footer links     | General/UI       | 1             | Click footer links   | Click    | Footer area           | Terms/Privacy/Support                            | Links open without error |               |        |       |              |


* Homepage loads successfully
* Header navigation links work (Flights, Hotels, Tours, Cars)
* Footer links (Terms, Privacy, Support) open correctly
* Responsive layout on mobile & desktop
* Broken link validation (no 404 pages)
* SSL certificate valid, no mixed content
* Performance baseline check (<3s homepage load)

---

## 2. User Registration & Login

| Sl. No. | DATE | Application | Test Case ID | Test Case Name      | Module       | Step No. | Step Description                | Action   | Element        | Input                 | Expected             | Actual | Status | Notes | Time |
| ------- | ---- | ----------- | ------------ | ------------------- | ------------ | -------- | ------------------------------- | -------- | -------------- | --------------------- | -------------------- | ------ | ------ | ----- | ---- |
| 1       |      | PHPTRAVELS  | UR-001       | Register valid user | Registration | 1        | Open registration page          | Open URL | Register link  | -                     | Page loads           |        |        |       |      |
|         |      |             |              |                     |              | 2        | Enter valid details             | Input    | Form fields    | Name, email, password | Registration success |        |        |       |      |
| 2       |      | PHPTRAVELS  | UR-002       | Existing email      | Registration | 1        | Submit form with existing email | Input    | Email field    | Used email            | Error shown          |        |        |       |      |
| 3       |      | PHPTRAVELS  | UR-003       | Login valid user    | Login        | 1        | Open login page                 | Open URL | Login link     | -                     | Page loads           |        |        |       |      |
|         |      |             |              |                     |              | 2        | Enter valid credentials         | Input    | Email/Password | Correct values        | Login success        |        |        |       |      |

### Registration

* Register with valid details → success email
* Register with existing email → validation error
* Register with invalid email format
* Register with weak password (if rules exist)
* Register with empty fields

### Login

* Login with valid credentials
* Login with incorrect password
* Login with blank fields
* Login with unregistered email
* Forgot‑password workflow (if available)

---

## 3. Hotels Module – Full Booking Flow

### Search

* Search hotels with valid location + dates
* Search with invalid range (checkout < check‑in)
* Search with today as check‑in
* Search with long stay (boundary testing)
* Search with blank fields

### Results

* Hotel card shows correct price, rating, room info
* Filters (stars, price range, amenities) apply correctly
* Sorting (high→low price, rating) works

### Booking

* Select hotel → room details page loads
* Book Now → booking form loads
* Enter valid guest info → proceed
* Payment successful → confirmation shown + email
* Payment failed → error + retry option
* Booking cancel (if supported)
* Modify booking (change dates)

---

## 4. Flights Module – Full Booking Flow

### Search

* Valid flight search (origin, destination, dates)
* Invalid route selection
* Return date < departure
* Past dates
* Extreme future dates (boundary)

### Booking

* Select flight → fare rules display
* Choose seats, baggage (if applicable)
* Enter passenger details
* Payment success / failure
* Email confirmation

---

## 5. Tours Module

### Search

* Search tours by location
* Filter by category (Adventure, Family, etc.)
* Sort by price

### Booking

* View tour details (gallery, itinerary)
* Select date
* Check availability (capacity scenarios)
* Add extras (guide, transport)
* Valid & invalid payment

---

## 6. Cars Module

### Search

* Search with pickup/drop‑off dates and times
* Invalid ranges
* Filters by vehicle type, transmission, seats

### Booking

* Select car → details page
* Add-ons (insurance, GPS)
* Payment workflow
* Cancel/modify booking

---

## 7. Admin / Dashboard (if accessible)

* Admin login
* Create/edit/delete hotel entries
* Create/edit/delete flight entries
* Create/edit/delete tours
* User list → activate/deactivate users
* Booking management → approve/reject/cancel
* Reports generation (bookings, revenue)
* Role-based access validation
* Audit trail checks

---

## 8. Payment Gateway Testing

* Valid credit card
* Invalid card number
* Expired card
* Empty fields
* High amount transactions
* Payment timeouts/network failure
* Retry payment flow

---

## 9. Negative Test Scenarios

* Enter special characters in textboxes (XSS attempts)
* SQL injection strings in input fields
* Extremely large values
* Navigating back during payment
* Session timeout during booking

---

## 10. Performance / Non‑Functional

* Load tests on hotel search
* Stress tests with rapid search requests
* Browser compatibility: Chrome, Firefox, Safari, Edge
* Mobile browser validation
* Accessibility (alt text, contrast, keyboard navigation)

---

## 11. Data Validation

* Required field validation
* Email, phone, postal code format checks
* Max length enforcement
* Duplicate booking reference validation
* Proper error message mapping

---

## 12. Suggested Excel Format

Use this header format in your spreadsheet for each test case:

Sl. No. | DATE | Application | Test Case ID | Test Case Name | Module / Feature | Test Step No. | Step Description | Keyword (Action) | Test Object / Element | Input Data | Expected Result | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed time

---


