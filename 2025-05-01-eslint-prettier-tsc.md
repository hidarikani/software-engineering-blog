# ESLint, Prettier, TSC

Setting up code linting and formatting is essential when starting a new web project. For JavaScript, the industry standard is ESLint, which has been widely used for years due to its extensibility. It provides a recommended rule set by default, but you can enhance it with plugins, such as one that supports React's JSX syntax.

At first glance, it might seem that if a project uses ESLint, then the code must be of high quality. However, upon closer inspection, ESLint’s configurability is both a strength and a weakness. Since there are countless ways to configure rules, projects that do not adhere to the default rule set often have vastly different configurations. As a result, the code quality between projects can vary significantly, depending on how ESLint has been set up.

Linting helps identify quality issues in code, even when the syntax is technically correct. A simple example in JavaScript is variable declarations. ESLint includes a rule that warns when a variable is declared but never reassigned and isn’t marked as a constant.

Apart from linting, which is meant to catch potential quality issues, a code formatter is also necessary. Formatting is primarily for human readability, ensuring a consistent style across files. Manually formatting a large file can be time-consuming, which is why automatic formatters, such as Prettier, were developed.

When working with TypeScript, things become even more complicated. TypeScript comes with its own compiler (TSC), which includes a built-in language service. This service is integrated into VS Code by default, meaning a fresh installation of VS Code already supports TypeScript without requiring additional plugins. The TypeScript language service highlights errors directly in the code editor.

ESLint supports TypeScript linting through plugins. However, Visual Studio Code relies on the TypeScript Compiler (TSC) language service to highlight errors. As a result, running ESLint in the CLI may produce different results from the errors displayed in the editor. To ensure consistency, you can configure the ESLint plugin in Visual Studio Code to lint TypeScript files directly and disable linting from the TypeScript language service.

> [!NOTE]
> Licensed under CC BY-NC 4.0