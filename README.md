# Web Automation Assessment - Sauce Demo E2E Tests

A comprehensive end-to-end testing project built with Playwright to automate interactions with the Sauce Demo web application. This project demonstrates best practices in web automation testing, including page interaction, form handling, and user workflow validation.

## Project Overview

This automation project tests the core functionality of the Sauce Demo application, which is a popular demo e-commerce site used for testing purposes. The tests validate the complete user journey from login to logout, including cart interactions.

## Features

- **Multi-browser testing**: Tests run on Chromium, Firefox, and WebKit browsers
- **Complete user flow**: Login, product selection, cart management, and logout
- **Visual validation**: Screenshots and traces for debugging
- **Comprehensive reporting**: HTML reports generated after test execution

## Tech Stack

- **Framework**: [Playwright](https://playwright.dev/) for robust browser automation
- **Language**: TypeScript
- **Testing**: End-to-End (E2E) testing scenarios
- **Reporting**: HTML reports with detailed execution logs

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Prince-71-Cloud/WebAutomationAssessment.git
   cd WebAutomationAssessment
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Scripts

The project includes the following npm scripts:

- `npm test` or `npm run playwright`: Run all Playwright tests
- `npm run report`: View the HTML test report

## Test Configuration

- **Test Directory**: `./tests`
- **Browsers**: Chromium, Firefox, WebKit
- **Report Format**: HTML
- **Trace Collection**: On first retry for failed tests
- **Parallel Execution**: Enabled for faster test runs

## Test Scenarios

The project currently includes one comprehensive test scenario:

- **Sauce Demo E2E Test**: Validates the complete user workflow including:
  - Successful login with valid credentials
  - Adding items to the shopping cart
  - Verifying cart contents
  - Navigating between pages
  - Logging out from the application

## Usage

To run the tests:

```bash
npm test
```

To run tests on a specific browser:

```bash
npx playwright test --project=chromium
```

To run tests in headed mode:

```bash
npx playwright test --headed
```

## Reports

After test execution, detailed HTML reports are generated in the `playwright-report` directory. You can view them by running:

```bash
npm run report
```

## Project Structure

```
├── tests/                    # Test files
│   └── assessment.spec.ts    # Main test file with E2E scenarios
├── playwright.config.js      # Playwright configuration
├── package.json              # Project dependencies and scripts
├── README.md                 # Project documentation
└── node_modules/             # Dependencies (not tracked in Git)
```

## Browser Support

- Chromium (Chrome, Edge)
- Firefox
- WebKit (Safari)

## Test Data

The tests use the standard Sauce Demo credentials:
- Username: `standard_user`
- Password: `secret_sauce`

## Troubleshooting

- If you encounter issues with browser dependencies, run:
  ```bash
  npx playwright install
  ```

- For detailed tracing when tests fail, check the trace files in the test-results directory.

## CI/CD Integration

This project includes a GitHub Actions workflow that automatically runs tests on every push and pull request to the main branch.

### GitHub Actions Workflow

The workflow:
- Runs tests on Ubuntu with Node.js 18
- Installs all dependencies and Playwright browsers
- Executes the Playwright tests across different browsers
- Uploads test results and reports as artifacts

To view the workflow runs, navigate to the "Actions" tab in your GitHub repository.

### Allure Report Visualizations

<img width="1896" height="813" alt="Report Overview" src="https://github.com/user-attachments/assets/774b90f7-d55c-44ca-b140-0fd812d3677d" />
<img width="1872" height="933" alt="Report Graph" src="https://github.com/user-attachments/assets/0b3aa185-a706-4734-a738-7925a2387fe7" />
<img width="1887" height="904" alt="Timeline" src="https://github.com/user-attachments/assets/ad07c7f3-266b-4217-adc5-0cedc07ecb68" />
<img width="1890" height="911" alt="Suites" src="https://github.com/user-attachments/assets/7a10bb58-a190-43f6-b23a-e374c56549fc" />





## License

This project is licensed under the ISC License.
