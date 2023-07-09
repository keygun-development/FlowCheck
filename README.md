# FlowCheck

FlowCheck is an open-source repository that automates the installation of packages and performs testing using ESLint and PHP_CodeSniffer when creating a Pull Request. This repository streamlines the workflow by integrating package management and code quality checks.

## Features

- Automated installation of npm packages and composer packages
- Testing JavaScript code with ESLint
- Testing PHP code with PHP_CodeSniffer
- Easy integration into your existing project workflows

## Prerequisites

Before getting started, ensure that you have the following prerequisites installed:

- Node.js (for npm package installation)
- PHP (for composer package installation and PHP_CodeSniffer)

## Installation

1. Clone this repository to your local machine:

   ```shell
   git clone https://github.com/your-username/FlowCheck.git
   ```
2. Change into the repository directory:
    ```shell
    cd FlowCheck
    ```
3. Install npm packages:

    ```shell
    npm install
    ```
4. Install composer packages:

    ```shell
    composer install
    ```
## Usage
1. Change the folders
   
   Change the commands in the `composer.json` and `package.json` to check the folders you want to be checked.
   For more information check: [ESLint Documentation](https://eslint.org/docs/latest/use/getting-started) & [PHPCS Documentation](https://github.com/slevomat/coding-standard)
2. Change the rules
   By default it uses the `ruleset.xml` and `.eslintrc.js` to set the rules for checking code standards. You may modify this to your own desire.
3. Run ESLint to perform JavaScript code linting:

    ```shell
    npm run lint
    ```
    This command will analyze your JavaScript files and report any linting errors or warnings.

3. Run PHP_CodeSniffer to check PHP code standards:

    ```shell
    composer run test
    ```
    This command will examine your PHP files according to predefined coding standards and display any violations found.

## Contributing
Contributions to FlowCheck are welcome! If you encounter any issues, have suggestions, or would like to contribute enhancements, please submit a pull request.