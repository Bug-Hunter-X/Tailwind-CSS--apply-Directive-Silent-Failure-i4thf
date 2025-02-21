# Tailwind CSS @apply Directive Silent Failure

This repository demonstrates a subtle bug in Tailwind CSS's `@apply` directive where using a non-existent or misspelled class results in a silent failure.  The styles are simply not applied without any error messages, making debugging more challenging.

## Bug Description
The `@apply` directive is a powerful tool, but it doesn't provide explicit error handling for invalid class names. If you attempt to apply a class that doesn't exist in your Tailwind configuration or make a typo, the directive silently ignores the invalid class.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` (if you have Node.js and npm installed).
3. Observe that the `bug.css` styles do not apply correctly. The expected styling from `.nonExistentClass` is missing.
4. Compare it with the solution in `bugSolution.css`.

## Solution
The solution involves carefully checking for typos and ensuring that all class names used with `@apply` exist in your Tailwind configuration (or are added correctly).

Careful attention to detail and effective use of your editor's linting or autocompletion features can prevent this type of error.

## Additional Notes
This silent failure can be difficult to track down, especially in larger projects.  Thorough testing and code review are essential for preventing this issue.