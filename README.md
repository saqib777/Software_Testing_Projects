<div align="center">
  
# Software Testing Projects
</div>

A collection of hands-on software testing projects I built while learning and strengthening core QA and SDET skills. Each project includes detailed test suites, scenario breakdowns, screenshots, and full documentation. Most of the work here is manual testing, supported by Katalon Studio for automation and validation.

## Badges

![Manual Testing](https://img.shields.io/badge/Testing-Manual-blue)
![Katalon Studio](https://img.shields.io/badge/Tool-Katalon-green)
![Status Active](https://img.shields.io/badge/Status-Active-success)
![GitHub Last Commit](https://img.shields.io/github/last-commit/saqib777/Software_Testing_Projects)

---

# Table of Contents

1. [Overview](#overview)
2. [Repository Structure](#repository-structure)
3. [Project Details](#project-details)
4. [Tools Used](#tools-used)
5. [How to Navigate This Repository](#how-to-navigate-this-repository)
6. [Unique Highlights](#unique-highlights)
7. [Future Roadmap](#future-roadmap)
8. [Notes for Recruiters](#notes-for-recruiters)
9. [About the Author](#about-the-author)

---

# Overview

This repository serves as my central portfolio of software testing work. Every folder represents a real application that I tested end-to-end — covering functional flows, validations, error conditions, and boundary cases.

It reflects how I approach testing: structured, thorough, and focused on real-world user journeys.

---

# Repository Structure

| Folder/File                   | Description                                                                                                                                          |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BookCart/**                 | Test cases for BookCart Azure Application, including registration and login scenarios.                                                               |
| **Basic-Calculator/**         | Manual test cases for TestSheepNZ Basic Calculator: input validation, arithmetic operations, and error handling.                                     |
| **ParaBank/**                 | Test documentation for ParaBank (customer flows) including login, transfers, account creation, and validations.                                      |
| **ParaBank_Admin_Testing.md** | Covers admin page testing such as configuration management, SOAP/JMS service validation, UI checks, and loan provider logic.                         |
| **Parking_Calculator.md**     | Full test suite for the Shino Parking Calculator: functional flows, rate validation, boundary conditions, date/time validation, and error scenarios. |
| **Presta-Shop/**              | Detailed test suite for PrestaShop demo store: product search, cart, checkout, payment, account creation, and negative test flows.                   |
| **Parasoft/**                 | Extensive testing of Parasoft demo site including account creation, workflows, UI testing, and validation rules.                                     |
| **Cloth-Shop/**               | Functional and UI testing of an eCommerce clothing store: product listing, filters, cart logic, and checkout.                                        |
| **PHPTravels/**               | Complete test suite for PHPTravels demo: booking workflows, authentication, validations, and UI checks.                                              |
| **shino-de-parkcalc/**        | Additional scenarios, rate rules, invalid flows, boundary testing for Shino Parking Calculator.                                                      |
| **README.md**                 | Project documentation.                                                                                                                               |

---

# Project Details

## BookCart

* Covered registration, login, input validation, UI checks, and error scenarios.
* Includes both positive and negative flows.

## Basic Calculator

* Arithmetic operations (addition, subtraction, multiplication, division).
* Input validation (blank fields, invalid characters, overflows).
* Error handling for divide-by-zero.

## ParaBank

* Customer-facing tests: login, transfers, bill payments, activity checks.
* Admin portal tests: configuration, JAXB/SOAP services, form validations.

## Parking Calculator

* Rate calculation logic testing.
* Time/date validation.
* Complex boundary conditions.
* Error messages and invalid-flow coverage.

## PrestaShop

* End-to-end eCommerce flow testing.
* Cart, checkout, discounts, address management.
* UI validations and negative scenarios.

## Parasoft

* Authentication, workflow validations, form testing.
* UI checks and data rule testing.

## Cloth Shop

* Product browsing, filtering, cart logic, checkout workflow.
* Validations and negative scenario coverage.

## PHPTravels

* Customer booking journey testing.
* Search and booking workflows.
* UI checks and validation rules.

---

# Tools Used

### Manual Testing

* Test case design (BVA, ECP, Decision Tables, Use Cases)
* Exploratory testing
* Negative scenario design

### Katalon Studio

* Web UI test automation
* Recording, object repository management
* Assertions and report exports

---

# How to Navigate This Repository

* Every folder contains a dedicated `TestCases.md` or equivalent.
* Files follow a consistent format:

  * Test Case ID
  * Test Scenario
  * Preconditions
  * Steps
  * Expected Result
  * Notes / Screenshots (if required)
* Some projects include additional subfolders like screenshots or workflows.

---

# Unique Highlights

* Over **150+ test cases** created across projects.
* Covers a mix of small apps, enterprise demos, and eCommerce platforms.
* Designed using real QA techniques: BVA, ECP, functional decomposition, and scenario mapping.
* Mix of **manual** and **Katalon** automation.
* Consistent formatting across all projects.
* Focus on thoroughness rather than minimal coverage.

---

# Future Roadmap

* Add Selenium WebDriver automation for major projects.
* Expand negative scenarios and integration test cases.
* Add CI/CD integration for automated test runs.
* Convert selected manual test suites into automated flows.

---

# Notes for Recruiters

* This repository reflects my practical approach to testing.
* I focus on clarity, strong coverage, and real-world user paths.
* Every project here is built independently as a learning and skill-building exercise.
* If you'd like to walk through any project during an interview, I'm happy to.

---

# About the Author

Hi, I'm **Mohammed Saqib**. I’m on a path toward becoming a strong SDET with solid foundations in manual testing, automation, and software quality principles.

I enjoy exploring different applications, breaking them, understanding edge cases, and designing clean, structured test suites. This repository documents that journey.

If you'd like to connect or collaborate, feel free to reach out!
