TypeScript & OOP — Module 4 Assignment 1
This repository contains solutions for the eight detailed programming problems included in the supplied assignment brief, along with two TypeScript learning blog posts.
Files
- [`solutions.ts`](./solutions.ts) — functions, generics, interfaces, tuple handling, class inheritance, and asynchronous validation.
- [`type-vs-interface.md`](./type-vs-interface.md) — differences between TypeScript type aliases and interfaces.
- [`type-narrowing.md`](./type-narrowing.md) — practical type narrowing with typeof, instanceof, and in.
Validation
The TypeScript solution is intended to compile in strict mode with an ES2020 target:
tsc --noEmit --strict --target ES2020 solutions.ts
Note About the Assignment Brief
The coding requirements also mention getUniqueNumbers, Product, and updateProductPrice, but the supplied problem descriptions do not include the specifications or sample behavior for these names. They have not been invented here. Confirm the missing problem statements with the instructor before final submission.
Submission
Create a public GitHub repository, add these files, and submit the repository URL as requested in the assignment instructions.