# Playwright Testing Samples with Typescript

The goal of this project was to put into practice my knowledge using this amazing tool for automation testing.

## The project 💻

The **SWAG Labs/Sauce Demo** store, from **Sauce Labs**, was automated using _TS + Playwright_. It generates an HTML report for passed and failed tests. Also, this project has **GitHub Action**s.

## Tools ⚙️

- _Playwright v1.28.1_.
- _GitHub Actions_.

## Main project structure 🗂️

```bash
.
├── .github/
│   └── workflows/
│       └── playwright.yml
├── pages/
│   ├── SLCartPage.ts
│   ├── SLCheckoutCompletePage.ts
│   ├── SLCheckoutInformationPage.ts
│   ├── SLCheckoutOverviewPage.ts
│   ├── SLLoginPage.ts
│   └── SLProductPage.ts
├── tests/
│   ├── login.spec.ts
│   ├── logout.spec.ts
│   └── shoppingCart.spec.ts
├── .env.template
├── package.json
└── playwright.config.ts
```

## Setup 🛠️

The following steps can be executed using a terminal (I use [hyper](https://hyper.is/)), or using the terminal provided by VS Code.

1. Clone the repo on your computer at any path you want.-

```bash
> git clone

```

2. In the path you cloned the repo, open the project folder and install the packages.-

```bash
> cd playwright-testing-samples

> npm i
```

3. Before to execute the tests, you need to create a _.env_ file at root level. There is a _.env.template_ file with the structure that should follow your _.env_ file. Just delete the _.template_ suffix and fill with the values you want to use.

   For demo purposes, you can fill it with these values.-

```bash
BASE_URL=https://www.saucedemo.com/

# Credentials

USERNAME=standard_user
PASSWORD=secret_sauce
INVALID_USERNAME=invalid_username
INVALID_PASSQORD=invalid_password
LOCKED_USERNAME=locked_out_user
```

## Run the tests ⚡

```bash
# If you want to just only run the tests, execute the following command:
> npm run execute:tests
# If you want to see a report of your executed tests, execute the following command:
> npm run execute:report

# If you want to execute the both commands above:
> npm run playwright:all
```

When you execute the command to see the report, a new folder is generated at root level (**playwright-report**). This folder contains the report for the executed tests.
