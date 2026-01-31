# Hacker News Sorting Validator

<img src="https://img.shields.io/badge/Playwright-2.x-45ba4b?logo=playwright&logoColor=white" alt="Playwright"> <img src="https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white" alt="Node.js"> <img src="https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black" alt="JavaScript"> <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">

## Overview

An automated testing solution that validates the sorting functionality of Hacker News articles. The test suite navigates through multiple pages, collects the first 100 articles, and verifies they are correctly sorted by published timestamp in descending order. Built using Playwright with best practices including Page Object Model, parallel execution, and CI/CD integration.

## About This Project

Developed as a technical assessment for the [QA Engineer role at QA Wolf](https://www.task-wolf.com/apply-qae), this project showcases proficiency in test automation, debugging, and software quality engineering. The assignment focused on real-world QA scenarios: building maintainable Playwright tests, effective debugging practices, and clear technical communication.

**Key Requirements Delivered:**

- ✓ Automated Playwright test suite in JavaScript
- ✓ Sorting validation across paginated data
- ✓ Page Object Model architecture
- ✓ CI/CD integration and reporting

[View QA Wolf role details →](https://www.task-wolf.com/apply-qae)

## Key Features

- ✅ **Automated Pagination** — Dynamically navigates through multiple pages to collect 100 unique articles
- ✅ **Sorting Validation** — Verifies articles are sorted by timestamp in descending order
- ✅ **Page Object Model** — Clean, maintainable architecture with reusable page components
- ✅ **Parallel Execution** — Optimized test runtime with concurrent test execution
- ✅ **CI/CD Ready** — GitHub Actions integration for automated testing
- ✅ **Comprehensive Reporting** — HTML reports with detailed test results and screenshots
- ✅ **Code Quality** — ESLint configuration for consistent code standards

## Tech Stack

- **Test Framework:** Playwright 2.x
- **Language:** JavaScript (ES6+)
- **Runtime:** Node.js 18+
- **Code Quality:** ESLint
- **CI/CD:** GitHub Actions

## Project Structure

```
├── pages/
│   └── HackerNewsPage.js          # Page Object Model implementation
├── tests/
│   └── hacker-news-sorting.spec.js # Main test suite
├── playwright.config.js            # Playwright configuration
├── eslint.config.mjs              # ESLint rules
└── .github/workflows/             # CI/CD pipeline
```

## Getting Started

### Prerequisites

- Node.js 18 or higher
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/LakinduQA/hacker-news-sorting-validator.git
cd hacker-news-sorting-validator

# Install dependencies
npm install

# Install Playwright browsers
npx playwright install
```

## Usage

### Running Tests

```bash
# Run all tests (headless)
npx playwright test

# Run with browser UI visible
npx playwright test --headed

# Run on specific browser
npx playwright test --project=chromium

# Run with retries for reliability
npx playwright test --retries=2
```

### View Test Reports

```bash
# Open HTML report
npx playwright show-report

# Run linting
npm run lint
```

## Important Notes

**Testing Against Live Data:** Hacker News is a live site with constantly changing content. Occasional test failures may occur due to:

- Articles being added/removed during test execution
- Network latency or temporary pagination issues
- Server-side caching behavior

The test suite includes retry logic to handle transient failures. For maximum reliability in CI/CD environments, use the `--retries` flag.

## License

MIT
