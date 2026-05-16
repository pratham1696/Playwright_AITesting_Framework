# Playwright AI Testing Framework

## Overview

This project demonstrates a complete **Software Testing Life Cycle (STLC)** automation pipeline using Playwright and AI concepts. It showcases the ability to execute end-to-end browser tests, parse test results, and automatically create defect reports in a mock Jira environment.

## Architecture

The framework handles the following sequence automatically:
```
Test Execution → Result Analysis → Defect Reporting → Summary
```

## Getting Started

### Prerequisites

Ensure you have Node.js installed, then install the dependencies:
```bash
npm install
```

### Run Automated Tests

To run the Playwright test suite only:
```bash
npm run test
```

### Run the Full Pipeline

1. In Terminal 1, start the mock Jira server:
```bash
npm run start-jira
```

2. In Terminal 2, run the full pipeline:
```bash
npm run run-pipeline
```

3. View the HTML report:
```bash
npm run report
```

## Features

- **Automated Execution:** 10 diverse Playwright tests covering authentication, visual checks, timeouts, and form interactions.
- **Defect Reporting:** Parses test results and automatically posts bugs to a local Jira mock server.
- **Reporting:** Uses Playwright's built-in reporters to generate comprehensive HTML and JSON reports.

## Project Structure

- `config/` - Global configuration and Jira mock settings.
- `tests/` - Playwright spec files.
- `mcp_scripts/` - Node.js scripts orchestrating the full pipeline.
- `jira_mock/` - A local express server mimicking a Jira REST API.
- `templates/` & `documents/` - Used for test case and test plan generation schemas.
