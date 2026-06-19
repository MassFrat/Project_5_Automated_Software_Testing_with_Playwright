## Project_5_Automated_Software_Testing_with_Playwright

## Getting Started

Install dependencies and the Playwright browsers:

\`\`\`bash
npm install
npx playwright install
\`\`\`


## Annotations

Playwright provides built-in annotations to control which tests run and how they're grouped.

#### `test.describe`

Groups related tests into a logical block. Useful for shared setup, readability, and scoping hooks.

#### `test.skip`

Marks a test (or group) to be skipped. Useful for known issues, flaky tests under investigation, or features not yet implemented.

#### `test.only`

Restricts the run to only the marked test(s). Great for local debugging — **should never be committed**, since CI will only run the marked tests.

## Tagging Tests

Tags let you group tests across files (e.g. `@smoke`, `@regression`, `@api`) and run only the subset you need.

## Hooks

Hooks run setup/teardown logic at different scopes. They can be defined at the top level or inside a `test.describe` block.

## Helpers

Helpers are reusable functions (or Page Object Model classes) that keep test files focused on *what* is being tested rather than *how*.

## Reporters

Reporters determine how test results are presented. Configure one or more in `playwright.config.ts`:

Common built-in reporters:

| Reporter | Use Case |
|----------|----------|
| `list`   | Default, human-readable console output |
| `dot`    | Compact output, good for CI logs |
| `html`   | Interactive HTML report with traces and screenshots |
| `json`   | Machine-readable output for custom tooling |
| `junit`  | Integrates with CI dashboards (Jenkins, Azure DevOps, etc.) |

View the HTML report after a run:

\`\`\`bash
npx playwright show-report
\`\`\`


## Pause Command

`page.pause()` halts execution and opens the Playwright Inspector, letting you step through actions, inspect locators, and resume manually. Invaluable for debugging.



