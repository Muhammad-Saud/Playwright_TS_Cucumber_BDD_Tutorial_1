# Playwright (TS binding) + Cucumber (BDD) Automation Tutorial

This repository provides a tutorial for setting up and utilizing Playwright and Cucumber for automation testing.

## Installation & Setup

1. **Install Visual Studio Code (Open Source) - IDE**

   Download and install Visual Studio Code from [here](https://code.visualstudio.com/).

   Also, you can refer to the [official documentation](https://code.visualstudio.com/docs/?dv=win) for more information.

   For installation guidance, you can watch the YouTube software installation guide [here](https://www.youtube.com/watch?v=CPmQwlycfGI).

2. **Install Node.js**

   Download and install Node.js from [here](https://nodejs.org/en).

   Follow these steps to add Node.js to your environment variables:
   
   1. Open the Control Panel (Click the Start button, then click Control Panel).
   2. Click User Accounts.
   3. Click Change my environment variables.
   4. Select PATH and click the Edit... button.
   5. At the end of the Path Variable value, add `;C:\Program Files\nodejs`.
   6. Click OK on the "Edit User Variable" window, then click OK on the "Environment Variables" window.
   7. Start a command prompt window (Start button, then type cmd into the search and hit enter).
   8. At the prompt (`C:\>`) type `npm` and hit enter; you should now see some help text (Usage: `npm <command>` etc.) rather than "npm is not recognized..."

3. **Create Folder For Your Project**

4. **Open Visual Studio Code**

5. **Open Created Folder**

6. **Install Extension - Playwright Test for VSCode v1.0.15**

7. **Shortcuts**

   - `CTRL + SHIFT + P` - For Recently Used Files - Install PlayWright
   - Open Terminal
   - It Will Install All Dependencies Libraries
   - Install Extension - Cucumber v1.7.0
   - Install Dependencies

      ```bash
      npm i @cucumber/cucumber -D
      npm i ts-node -D
	  npm i -D @playwright/test
      ```

## Project Structure

1. Create the following directories:

   - `src\test\features`
   - Add a `steps` folder inside `test`
   
2. Structure of directories:

   - `features` -> Simple English explanations of use cases
   - `steps` -> Actual Test Implementations (JavaScript Code)
   - Runner File -> To Execute Code -> .json Format

3. Go to the `features` folder and add a new file `Login.feature`.

4. Create a `cucumber.json` file in the root directory and paste the following code:

```json
{
    "default": {
            "formatOptions": {
                "snippetInterface": "async-await"
            },
        "paths": [
            "src/test/features/login.feature"
        ],
        "dryRun": false,
        "require": [
            "src/test/steps/*.ts"
        ],
        "requireModule": [
            "ts-node/register"
        ]
    }
}
```

## Test Application Details

- **Application URL:** https://bookcart.azurewebsites.net/login
- **Username:** Muhammad Saud
- **Password:** CComputing@12345

## Shortcuts and Tips

- `CTRL + J` -> Open Terminal
- `"ts-node/register"` -> To solve the TypeScript import statement error
- `CTRL + ,` -> User Defined Settings
- `CTRL + D` -> Find All Matching

## Important Notes

- "async and await make promises easier to write"
- `async` makes a function return a Promise
- `await` makes a function wait for a Promise

## Automation Tools

- Other Automation Tools:
  - Cypress
  - Selenium
  - Web Driver IO
  - Puppeteer (Chromium - Google)
  - Playwright (Microsoft)

## Auto-Wait BuiltIn

- No `Thread.Sleep`
- No Implicit Wait
- No Explicit Wait

## Playwright Official Documentation from (https://playwright.dev/).

---

Feel free to contribute to this tutorial and make it better! If you have any questions, feel free to open an issue or reach out to us. Happy testing!


