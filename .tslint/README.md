# About this file structure

Rules are split into categories defined in the [documentation][tslint rules].

**Note:** Rules that require type checking are disabled,
since this feature is not supported by every IDE.
Those rules are listed below (in each category).

[tslint rules]: https://palantir.github.io/tslint/rules/


## ts-specific.tslint.json

TypeScript Specific rules find errors related to TypeScript features.

**Rules that are disabled because they require type checking:**

- [promise-function-async](https://palantir.github.io/tslint/rules/promise-function-async/)

## functionality.tslint.json

Functionality rules catch common errors in JS programming or otherwise
confusing constructs that are prone to producing bugs.

**Rules that are disabled because they require type checking:**

- [no-for-in-array](https://palantir.github.io/tslint/rules/no-for-in-array/)

## maintainability.tslint.json

Maintainability rules make code maintenance easier.

## style.tslint.json

Style rules enforce consistent style across your codebase.
