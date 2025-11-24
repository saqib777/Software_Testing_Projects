# SHOP - Testing   

## Website Link - https://shop.polymer-project.org

This test suite has been designed to validate the functionality, usability, and reliability of the Polymer Project Demo Shop (https://shop.polymer-project.org). The site is a sample e-commerce application built using Polymer components, intended to showcase modern web application architecture and responsive design.

The objective of this test suite is to:
- Ensure that core modules (Home, Product Listing, Cart, Checkout, and UI/UX) function as expected.
- Verify that user interactions such as navigation, product selection, cart updates, and checkout flows behave correctly.
- Confirm that the application provides a consistent and responsive experience across different devices and screen sizes.
- Identify potential issues in routing, data rendering, and state management.

Scope:
- Functional testing of navigation, product listing, cart operations, and checkout flow.
- UI/UX validation for responsiveness and layout consistency.
- Negative scenarios such as empty cart behavior.
- Exclusions: Payment gateway and backend order processing, as the demo site does not implement real transactions.

Approach:
- Manual execution of test cases using the provided template.
- Each test case includes step-by-step actions, expected results, and placeholders for actual results and status.
- Elapsed time is estimated for manual testing purposes.


Sl. No. | DATE       | Application | Test Case ID | Test Case Name              | Module / Feature | Test Step No. | Step Description                          | Keyword      | Test Object / Element           | Input Data                  | Expected Result                                                                 | Actual Result | Status | Notes                          | Elapsed time
--------|------------|-------------|---------------|-----------------------------|------------------|---------------|-------------------------------------------|--------------|---------------------------------|-----------------------------|---------------------------------------------------------------------------------|---------------|--------|--------------------------------|--------------
1       | 24-Nov-25  | SHOP        | TC-HOME-001   | Verify Home Page Load       | Home             | 1             | Navigate to site URL                      | Navigation   | Browser URL bar                 | https://shop.polymer-project.org | Home page loads with header, footer, and navigation links visible                |               |        | Basic availability check       | 1 min
2       | 24-Nov-25  | SHOP        | TC-HOME-002   | Verify Navigation Links     | Home             | 1             | Click “SHOP” link in header               | Link Click   | Header navigation link          | SHOP link                   | Redirects to product listing page                                                |               |        |                                | 2 min
3       | 24-Nov-25  | SHOP        | TC-LIST-001   | Verify Product Listing Page | Product Listing  | 1             | Navigate to /list                         | Navigation   | Product listing page            | URL: /list                  | Product grid loads with multiple items, each showing image, title, and price     |               |        |                                | 2 min
4       | 24-Nov-25  | SHOP        | TC-LIST-002   | Verify Product Details      | Product Listing  | 1             | Click on a product                        | Link Click   | Product card                    | Any product                 | Product detail page opens with description, price, and “Add to Cart” button      |               |        |                                | 3 min
5       | 24-Nov-25  | SHOP        | TC-CART-001   | Add Product to Cart         | Cart             | 1             | Click “Add to Cart” on product detail     | Button Click | Add to Cart button              | Product ID                  | Cart icon updates with item count                                                 |               |        |                                | 2 min
6       | 24-Nov-25  | SHOP        | TC-CART-002   | Verify Cart Page            | Cart             | 1             | Navigate to /cart                         | Navigation   | Cart page                       | URL: /cart                  | Cart page shows added products with quantity and total price                     |               |        |                                | 2 min
7       | 24-Nov-25  | SHOP        | TC-CART-003   | Update Quantity in Cart     | Cart             | 1             | Change product quantity                   | Input Change | Quantity field                  | Quantity = 2                | Cart updates total price accordingly                                             |               |        |                                | 3 min
8       | 24-Nov-25  | SHOP        | TC-CHECK-001  | Proceed to Checkout         | Checkout         | 1             | Click “Checkout” button                   | Button Click | Checkout button                 | Cart with items             | Redirects to checkout page (demo may show placeholder)                           |               |        | Demo site may not support full checkout | 2 min
9       | 24-Nov-25  | SHOP        | TC-CHECK-002  | Verify Empty Cart Behavior  | Checkout         | 1             | Navigate to /cart with no items           | Navigation   | Cart page                       | Empty cart                  | Cart page displays “No items in cart” message                                    |               |        |                                | 1 min
10      | 24-Nov-25  | SHOP        | TC-UI-001     | Verify Responsive Layout    | UI/UX            | 1             | Resize browser window                     | Resize       | Page layout                     | Different screen sizes      | Layout adjusts responsively (grid collapses, menu adapts)                        |               |        |                                | 4 min
11      | 24-Nov-25  | SHOP        | TC-SEARCH-001 | Verify Product Search           | Search           | 1             | Enter keyword in search bar               | Input        | Search bar                      | "Shoes"                     | Product listing updates to show only relevant items                              |               |        |                                | 3 min
12      | 24-Nov-25  | SHOP        | TC-FILTER-001 | Verify Category Filter          | Product Listing  | 1             | Select category filter                    | Filter       | Category dropdown               | "Men’s Clothing"            | Product listing updates to show only items in selected category                  |               |        |                                | 3 min
13      | 24-Nov-25  | SHOP        | TC-FILTER-002 | Verify Price Filter             | Product Listing  | 1             | Apply price filter                        | Filter       | Price filter slider              | Range: $10–$50              | Product listing updates to show only items within price range                    |               |        |                                | 3 min
14      | 24-Nov-25  | SHOP        | TC-CHECK-003  | Validate Checkout Form Fields   | Checkout         | 1             | Enter invalid email in checkout form      | Input        | Email field                     | "abc@xyz"                   | Error message displayed for invalid email format                                |               |        |                                | 4 min
15      | 24-Nov-25  | SHOP        | TC-CHECK-004  | Validate Mandatory Fields       | Checkout         | 1             | Leave address field blank                 | Input        | Address field                   | Empty                       | Error message displayed prompting user to fill mandatory field                   |               |        |                                | 4 min
16      | 24-Nov-25  | SHOP        | TC-PERF-001   | Verify Page Load Performance    | Performance      | 1             | Measure load time for product listing     | Performance  | Product listing page            | URL: /list                  | Page loads within 3 seconds                                                      |               |        | Performance benchmark           | 5 min
17      | 24-Nov-25  | SHOP        | TC-ACCESS-001 | Verify Accessibility Features   | Accessibility    | 1             | Navigate site using keyboard only         | Accessibility| Navigation links, buttons       | Tab/Enter keys              | All interactive elements accessible via keyboard navigation                      |               |        |                                | 6 min
18      | 24-Nov-25  | SHOP        | TC-ACCESS-002 | Verify Screen Reader Support    | Accessibility    | 1             | Use screen reader on product listing      | Accessibility| Product listing page            | Screen reader enabled       | Product titles, prices, and buttons announced correctly                          |               |        |                                | 6 min



TC-HOME-001: Verify Home Page Load
- Purpose: Ensure the site is accessible and loads correctly.
- Steps: Open URL in browser.
- Expected: Header, footer, and navigation links visible.
- Risks: Site downtime or slow load.

TC-HOME-002: Verify Navigation Links
- Purpose: Confirm header navigation works.
- Steps: Click “SHOP” link.
- Expected: Redirect to product listing.
- Risks: Broken links or incorrect routing.

TC-LIST-001: Verify Product Listing Page
- Purpose: Validate product grid rendering.
- Steps: Navigate to /list.
- Expected: Multiple products displayed with image, title, price.
- Risks: Missing product data or broken layout.

TC-LIST-002: Verify Product Details
- Purpose: Ensure product detail page loads correctly.
- Steps: Click on any product card.
- Expected: Detail page shows description, price, Add to Cart button.
- Risks: Broken product links or missing details.

TC-CART-001: Add Product to Cart
- Purpose: Validate cart functionality.
- Steps: Click “Add to Cart” on product detail.
- Expected: Cart icon updates with item count.
- Risks: Cart not updating or item not added.

TC-CART-002: Verify Cart Page
- Purpose: Ensure cart page displays items.
- Steps: Navigate to /cart.
- Expected: Items listed with quantity and total price.
- Risks: Incorrect totals or missing items.

TC-CART-003: Update Quantity in Cart
- Purpose: Confirm cart updates correctly.
- Steps: Change product quantity to 2.
- Expected: Total price recalculated.
- Risks: Quantity change not reflected.

TC-CHECK-001: Proceed to Checkout
- Purpose: Validate checkout navigation.
- Steps: Click “Checkout” button.
- Expected: Redirect to checkout page (demo placeholder).
- Risks: Checkout page not loading.

TC-CHECK-002: Verify Empty Cart Behavior
- Purpose: Ensure empty cart message appears.
- Steps: Navigate to /cart with no items.
- Expected: “No items in cart” message displayed.
- Risks: Incorrect empty state handling.

TC-UI-001: Verify Responsive Layout
- Purpose: Validate responsive design.
- Steps: Resize browser window to mobile/tablet/desktop.
- Expected: Layout adapts (grid collapses, menu adapts).
- Risks: Poor responsiveness on certain screen sizes.

- TC-SEARCH-001: Verify Product Search
- Purpose: Ensure search functionality filters products correctly.
- Steps: Enter keyword "Shoes" in search bar.
- Expected: Product listing updates to show only relevant items.
- Risks: Search may return incorrect or no results.

TC-FILTER-001: Verify Category Filter
- Purpose: Validate category filter functionality.
- Steps: Select "Men’s Clothing" from category dropdown.
- Expected: Product listing updates to show only items in selected category.
- Risks: Incorrect filtering or empty results.

TC-FILTER-002: Verify Price Filter
- Purpose: Confirm price filter works correctly.
- Steps: Apply price range $10–$50.
- Expected: Product listing updates to show only items within range.
- Risks: Items outside range may appear.

TC-CHECK-003: Validate Checkout Form Fields
- Purpose: Ensure checkout form validates email format.
- Steps: Enter invalid email "abc@xyz".
- Expected: Error message displayed for invalid email.
- Risks: Form may accept invalid data.

TC-CHECK-004: Validate Mandatory Fields
- Purpose: Confirm mandatory fields are enforced.
- Steps: Leave address field blank.
- Expected: Error message prompts user to fill mandatory field.
- Risks: Checkout may proceed with incomplete data.

TC-PERF-001: Verify Page Load Performance
- Purpose: Measure performance of product listing page.
- Steps: Navigate to /list and record load time.
- Expected: Page loads within 3 seconds.
- Risks: Slow performance impacting user experience.

TC-ACCESS-001: Verify Accessibility Features
- Purpose: Ensure site is usable via keyboard navigation.
- Steps: Use Tab/Enter keys to navigate.
- Expected: All interactive elements accessible via keyboard.
- Risks: Elements not reachable or focus not visible.

TC-ACCESS-002: Verify Screen Reader Support
- Purpose: Validate accessibility for visually impaired users.
- Steps: Use screen reader on product listing page.
- Expected: Product titles, prices, and buttons announced correctly.
- Risks: Missing or incorrect ARIA labels.
