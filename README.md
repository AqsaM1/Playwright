# 🎭 Playwright Test Automation Project

This repository is a test automation framework using [Playwright](https://playwright.dev/), supporting end-to-end and API testing across Chromium, Firefox, and WebKit.


## 📦 Step-by-Step Setup & Usage

### 1️⃣ Install Node.js (if not already installed)

Download from: https://nodejs.org/


### 2️⃣ Initialize the Project

```bash
npm init -y

----
###3️⃣ Install Playwright and Required Browsers

npm install -D @playwright/test
npx playwright install

### 4️⃣ Run all tests
npx playwright test

### Run single test
npx playwright test tests/example.spec.ts

### Run a test by name
npx playwright test -g "homepage has correct title"


### 5️⃣ Run with Browser UI (headed)

npx playwright test --headed

### Run in headless mode
npx playwright test --headless


### 6️⃣ Run Tests in Different Browsers
npx playwright test --project=chromium
npx playwright test --project=firefox

### Make sure your playwright.config.ts has this:

projects: [
  { name: 'chromium', use: { browserName: 'chromium' } },
  { name: 'firefox', use: { browserName: 'firefox' } },
  { name: 'webkit', use: { browserName: 'webkit' } },
],


### 7️⃣ Folder Structure
playwright-project/
├── tests/                 # All test files here
│   └── example.spec.ts
├── playwright.config.ts   # Global test configuration
├── package.json
└── README.md

