# 🎭 Playwright Test Automation Project

This repository is a test automation framework using [Playwright](https://playwright.dev/), supporting end-to-end and API testing across Chromium, Firefox, and WebKit.

---

## 📦 Step-by-Step Setup & Usage

### 1️⃣ Install Node.js (if not already installed)

Download and install from: [https://nodejs.org](https://nodejs.org)

Verify installation:

```bash
node -v
npm -v

### 2️⃣ Initialize the Project
npm init -y

### 3️⃣ Install Playwright and Required Browsers

npm install -D @playwright/test
npx playwright install

### 4️⃣ Run All Tests

npx playwright test

### 5️⃣ Run a Single Test File

npx playwright test tests/example.spec.ts


### 6️⃣ Run a Test by Name

npx playwright test -g "homepage has correct title"

### 7️⃣ Run with Browser UI (Headed Mode)

npx playwright test --headed

### 8️⃣ Run in Headless Mode (default)

npx playwright test --headless

### 9️⃣ Run Tests in Specific Browsers

npx playwright test --project=chromium
npx playwright test --project=firefox
npx playwright test --project=webkit

### Make sure your playwright.config.ts includes:

projects: [
  { name: 'chromium', use: { browserName: 'chromium' } },
  { name: 'firefox', use: { browserName: 'firefox' } },
  { name: 'webkit', use: { browserName: 'webkit' } },
],

### 🔟 Folder Structure

playwright-project/
├── tests/                 # All test files here
│   └── example.spec.ts
├── playwright.config.ts   # Global test configuration
├── package.json
└── README.md
