## Playwright E2E Suite (TypeScript)

This repo is a sample end-to-end test framework built with **Playwright + TypeScript**, with test flows for **ZeroWebApp** (login, payments, funds, feedback, search, exchange, transactions).

### Setup

1. Clone:

```bash
git clone https://github.com/rithwik-01/E2E-Test-Suite.git
```

2. Install dependencies:

```bash
npm install
```

### Run tests
There are E2E tests for **ZeroWebApp** ([http://zero.webappsecurity.com](http://zero.webappsecurity.com)), grouped by flows like **payments**, **searchbox**, and more. To run them, use these npm scripts:

* `test:e2e` (all suites, all browsers)
* `test:e2e:exchange`
* `test:e2e:feedback`
* `test:e2e:funds`
* `test:e2e:login`
* `test:e2e:payments`
* `test:e2e:searchbox`
* `test:e2e:transactions`

* Run everything (all browsers):

```bash
npm run test:e2e
```

* Run a specific flow (example: funds):

```bash
npm run test:e2e:funds
```

Available flows: `exchange`, `feedback`, `funds`, `login`, `payments`, `searchbox`, `transactions`.

### Customize runs

Use Playwright directly:

```bash
npx playwright test
```

Example: run only payments on Firefox:

```bash
npx playwright test --project=firefox --grep @payments
```

Run headed:

```bash
npx playwright test --headed
```

### Reports and artifacts

* Screenshots/videos: `test-results/`
* HTML report: `playwright-report/`
* Open report:

```bash
npx playwright show-report
```