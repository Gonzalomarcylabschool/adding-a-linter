# Adding a linter

Adding a linter to your Node.js project is a good practice as it helps maintain consistent code style, catch potential errors, and improve overall code quality. Here's how you can add ESLint to your Node.js project.

## Initialize Your Node.js Project

If you haven't already initialized your Node.js project, create a new directory for your project and navigate into it using the terminal. Run the following command to initialize your project and create a `package.json` file:

```bash
npm init -y
```
## Install ESLint Locally

Install ESLint as a local project dependency using `npm`. This way, ESLint, and its configurations are specific to your project:

```bash
npm install eslint --save-dev
```

## Create ESLint Configuration

Create an ESLint configuration file named `.eslintrc.js` in your project's root directory. We will be using the popular Airbnb JavaScript style guide. We will install it using the following command: 

```bash
npx install-peerdeps --dev eslint-config-airbnb-base
```

In the `.eslintrc.js` file, add the following content. 

```js
module.exports = {
  extends: 'airbnb-base',
};
```

To have some super clean code, you can add the following instead: 

```js
module.exports = {
  env: {
    browser: true,
    es2021: true,
    jest: true,
  },
  extends: 'airbnb-base',
  overrides: [
  ],
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
  },
  rules: {
    'no-console': 'off',
    'object-curly-newline': 'off',
    'no-plusplus': 'off',
    'no-promise-executor-return': 'off',
    'func-style': 2,
    'arrow-body-style': 'off',
    quotes: ['error', 'single', { allowTemplateLiterals: true, avoidEscape: true }],
    'consistent-return': 'off',
    'no-alert': 'off',
    'no-unused-expressions': ['error', { allowTernary: true }],
    'no-unused-vars': ['error', { argsIgnorePattern: '_', destructuredArrayIgnorePattern: '^_' }],
  },
};

```
## Enjoy your clean code!

This will hopefully give you some nice looking code that you can be proud to show off to your friends family and potential employers. 
