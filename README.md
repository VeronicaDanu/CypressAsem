## Overview

**cypressAsem** is a scalable and maintainable Cypress framework for end-to-end testing using the Cucumber preprocessor. It supports BDD-style feature files, modular step definitions, and generates clean test reports using Mochawesome.

## Features

* Cypress with [Cucumber syntax](https://cucumber.io/docs/gherkin/)
* Gherkin-based feature files for business-readable tests
* Modular structure for organizing tests and logic
* Automated report generation (JSON + HTML via Mochawesome)
* Supports Chrome browser for headed test runs
* TypeScript support for step definitions

## Directory Structure

```
cypressAsem/
├── cypress/
│   ├── downloads/                 # File downloads (if any)
│   ├── e2e/
│   │   ├── features/              # Gherkin feature files
│   │   │   ├── login.feature
│   │   │   ├── products.feature
│   │   │   └── wishList.feature
│   │   ├── login/                 # Custom login-related tests or utilities
│   │   ├── products/              # Custom product-related tests or utilities
│   │   └── step_definitions/      # Cucumber step definitions (JS/TS)
│   ├── fixtures/                  # Test data (JSON)
│   ├── reports/                   # Test and report outputs
│   ├── screenshots/               # Screenshots from test failures
│   └── support/                   # Support files and custom commands
├── cypress.config.ts             # Cypress configuration (TypeScript)
├── .gitignore
├── package.json
└── README.md
```

## Installation

To install and set up the project locally:

```bash
git clone https://github.com/VeronicaDanu/CypressAsem.git
cd cypressAsem
npm install
```

## Running Tests

Run tests in **Chrome browser (headed mode)**:

```bash
npm run rulareCh
```

This will execute all `.feature` tests using the step definitions configured in `cypress/e2e/step_definitions`.

## Generating Reports

To **run all tests and automatically generate an HTML report**:

```bash
npm run runAndReport
```

This script will:

1. Run all tests in Chrome.
2. Merge `.json` test results using `mochawesome-merge`.
3. Generate an HTML report using `mochawesome-report-generator`.

📂 The final report will be located here:

```
cypress/reports/merged-html-report/merged-report.html
```

You can open this file in any web browser to view the test summary, errors, and screenshots.

## Notes

* **Feature files** should reside in `cypress/e2e/features/`
* **Step definitions** must be placed under `cypress/e2e/step_definitions/`
* The framework uses TypeScript for step definitions and supports `*.ts` files.

## Contributing

Contributions are welcome! Please follow good practices for pull requests and check for linting or formatting issues.

## Contact

For any questions or suggestions, feel free to reach out at [danu.veronica@ase.md].

