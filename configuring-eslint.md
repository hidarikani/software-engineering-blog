# Configuring ESLint

Common code quality issues that affect most codebases have been extensively documented by the developer community. Detecting and, in some cases, automatically fixing these issues is made possible by tools known as linters.

The most popular linter for JavaScript is ESLint. Installing ESLint is straightforward, but configuring it can introduce some complexity due to its flexibility and wide range of options. ESLint supports various rule sets (presets), depending on the technologies and syntax used in your project:

✅ Vanilla JavaScript​: The specific rule set depends on the ECMAScript version you target.
✅ JSX: When working with React, JSX support is essential.
✅ TypeScript: ESLint can be configured to lint TypeScript code with or without type checking. Type-aware linting provides more accurate results but can significantly slow down linting in large projects.

Another important aspect of linting is understanding the runtime environments involved. In modern single-page applications (SPAs), JavaScript is used both in the browser and in development tooling like automated tests. However, different environments expose different global variables and APIs. For example:

✅ Node.js (commonly used for tests and tooling) provides APIs like `fs` (file system) but lacks browser-specific globals like `window` or `document`.
✅ Browsers (where the app runs) support DOM-related globals but do not include Node-specific modules.

This distinction matters for linting. ESLint can be configured to recognize the
correct set of globals for each environment:

✅ For browser code, configure ESLint to recognize browser globals like window, document, etc.
✅ For test files running in Node configure ESLint to recognize Node globals and the testing framework’s global API (like describe, it, expect).

> [!NOTE]
> Licensed under CC BY-NC 4.0
