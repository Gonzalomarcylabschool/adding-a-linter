# Adding a linter

Adding a linter to your Node.js project is a good practice as it helps maintain consistent code style, catch potential errors, and improve overall code quality. Here's how you can add ESLint to your Node.js project.

## Initialize Your Node.js Project

If you haven't already initialized your Node.js project, create a new directory for your project and navigate into it using the terminal. Run the following command to initialize your project and create a package.json file:

```bash
npm init -y
```
## Install ESLint Locally

Install ESLint as a local project dependency using npm. This way, ESLint and its configurations are specific to your project:

```bash
npm install eslint --save-dev
```

## Create ESLint Configuration

Create an ESLint configuration file named .eslintrc.js in your project's root directory. We will be using the popular Airbnb JavaScript style guide. We will install it using the following command: 

```bash
npx install-peerdeps --dev eslint-config-airbnb-base
```