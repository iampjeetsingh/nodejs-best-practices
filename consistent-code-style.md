Here are some best practices for achieving consistent code style:

### 1. Choose a Style Guide: 
Select a style guide that aligns with your project's requirements and coding preferences. Airbnb and Standard.js are two widely used JavaScript style guides, but there are others available as well. The chosen style guide will serve as the foundation for your code style consistency.

### 2. Install ESLint: 
Set up ESLint in your project by installing it as a development dependency. You can do this by running the following command in your project's root directory:

```bash
npm install eslint --save-dev
```

### 3. Configure ESLint: 
Create an ESLint configuration file (e.g., .eslintrc.json) in your project's root directory. This file allows you to customize ESLint's rules and configurations according to your chosen style guide. You can start with a pre-defined configuration provided by the style guide or tailor it to your specific needs.

Example:
Here is a sample ESLint configuration file for the Airbnb style guide:
```json
{
  "extends": "airbnb"
}

```

### 4. Integrate Style Guide: 
Install the ESLint plugin or package associated with your chosen style guide. For example, if you're using the Airbnb style guide, you can install the eslint-config-airbnb package. This package includes the necessary ESLint rules and configurations to enforce the Airbnb style guide.
```bash
npm install eslint-config-airbnb --save-dev
```

### 5. Editor Integration: 
Configure your code editor or IDE to integrate with ESLint. Most popular editors have ESLint extensions or plugins available that can automatically highlight code style violations as you write code. This helps you identify and fix issues in real-time.

Example:
For Visual Studio Code, install the ESLint extension and enable it in your workspace settings:
```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}

```

### 6. Automate Code Formatting: 
Combine ESLint with a code formatter like Prettier to automate code formatting. Prettier can automatically format your code according to the rules defined in your ESLint configuration. This ensures consistent code style and saves time by eliminating manual formatting efforts.

Example:
1. Install Prettier and the ESLint plugin for Prettier by running the following command:
```bash
npm install prettier eslint-plugin-prettier --save-dev
```
2. Configure ESLint to use Prettier by adding the following to your ESLint configuration:
```json
{
  "extends": [
    "airbnb",
    "plugin:prettier/recommended"
  ]
}
```

### 7. Enforce Code Style: 
Make it a part of your development process to run ESLint and check for code style violations. You can set up pre-commit hooks or integrate ESLint into your continuous integration (CI) pipeline to prevent code with style violations from being committed or deployed.

Example:
Add an ESLint script to your project's package.json file to run ESLint:
```json
{
  "scripts": {
    "lint": "eslint ."
  }
}
```

### 8. Team Collaboration: 
Encourage all team members to follow the agreed-upon code style guidelines. Conduct code reviews to ensure adherence to the style guide and provide feedback to improve code quality and consistency.

By following these best practices, you can establish and maintain a consistent code style throughout your project, leading to cleaner, more readable, and maintainable code.