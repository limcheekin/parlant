This is the main repo of Parlant (https://parlant.io).

Parlant is a Python based agent framework. Its core strengths:

1. It allows you to create compliant and controlled AI agents for customer-facing use cases
2. It provides many conversational management features out of the box
3. It's built for enterprise, large-scale use cases, where SLAs, stability and security are paramount

The repo's structure follows the Hexagonal Architecture (Ports and Adapters) approach.

- src/parlant
  - core: Core framework code
  - adapters: Implementations of interfaces using 3rd party tools
  - api: REST API layer using FastAPI. Uses modules from core/
- tests: all tests for the project. Structure strives to mirror that which is under src/parlant.

General Coding Instructions:

- Always ensure you stick to Hexagonal Architecture patterns in line with how they're used in this codebase.
- Every time you add something, look for similar things in the codebase and ensure you follow the coding style.
- We use MyPy on strict mode. Every parameter needs to be type-annotated. Every function's result too.
- If you need to add a test for something, first say where you plan to add it and ask for confirmation.
- We follow TDD. When you make a change, first create a failing test. Once it fails, implement just enough so it passes.
- If you need to test classes/methods in sdk.py (or generally to test things that relate to engine behavior) make sure you inherit from SDKTest and understand how it works and how to use it.
- Test names should go "test*that*..." using clear names that explain the context, what is executed, and what is the expected result.
- You can run tests using pytest. Make sure you run "uv run pytest tests/path/to/test/file.py" while also specifying the test name that you need to run.

Always follow this plan when asked to code a feature or fix a bug:

1. Consider the codebase's structure
2. Describe your implementation plan, including:
   a. What tests you will write (test names + files they would live in)
   b. Why do you think the tests would initially fail
   c. Where you would plan to implement the code that would make the tests pass
3. Ask for plan confirmation. If you get feedback, revise your plan and ask for confirmation again until you get it.
4. Implement the tests first. Ask for confirmation and code review.
5. Once tests are approved, once again suggest your implementation plan for making them pass, and get plan review until confirmation.
6. Once your implementation plan is confirmed, go ahead with implementing the code to pass them.
7. Make sure to format all of the files you changed using ruff (it is installed in the environment).
8. Run `uv run python scripts/lint.py --mypy --ruff` to ensure your code has no lint issues.

<!-- gitnexus:start -->
# GitNexus — Code Intelligence

This project is indexed by GitNexus as **parlant** (19674 symbols, 31605 relationships, 227 execution flows). Use the GitNexus MCP tools to understand code, assess impact, and navigate safely.

> If any GitNexus tool warns the index is stale, run `npx gitnexus analyze` in terminal first.

## Always Do

- **MUST run impact analysis before editing any symbol.** Before modifying a function, class, or method, run `gitnexus_impact({target: "symbolName", direction: "upstream"})` and report the blast radius (direct callers, affected processes, risk level) to the user.
- **MUST run `gitnexus_detect_changes()` before committing** to verify your changes only affect expected symbols and execution flows.
- **MUST warn the user** if impact analysis returns HIGH or CRITICAL risk before proceeding with edits.
- When exploring unfamiliar code, use `gitnexus_query({query: "concept"})` to find execution flows instead of grepping. It returns process-grouped results ranked by relevance.
- When you need full context on a specific symbol — callers, callees, which execution flows it participates in — use `gitnexus_context({name: "symbolName"})`.

## Never Do

- NEVER edit a function, class, or method without first running `gitnexus_impact` on it.
- NEVER ignore HIGH or CRITICAL risk warnings from impact analysis.
- NEVER rename symbols with find-and-replace — use `gitnexus_rename` which understands the call graph.
- NEVER commit changes without running `gitnexus_detect_changes()` to check affected scope.

## Resources

| Resource | Use for |
|----------|---------|
| `gitnexus://repo/parlant/context` | Codebase overview, check index freshness |
| `gitnexus://repo/parlant/clusters` | All functional areas |
| `gitnexus://repo/parlant/processes` | All execution flows |
| `gitnexus://repo/parlant/process/{name}` | Step-by-step execution trace |

## CLI

| Task | Read this skill file |
|------|---------------------|
| Understand architecture / "How does X work?" | `.claude/skills/gitnexus/gitnexus-exploring/SKILL.md` |
| Blast radius / "What breaks if I change X?" | `.claude/skills/gitnexus/gitnexus-impact-analysis/SKILL.md` |
| Trace bugs / "Why is X failing?" | `.claude/skills/gitnexus/gitnexus-debugging/SKILL.md` |
| Rename / extract / split / refactor | `.claude/skills/gitnexus/gitnexus-refactoring/SKILL.md` |
| Tools, resources, schema reference | `.claude/skills/gitnexus/gitnexus-guide/SKILL.md` |
| Index, status, clean, wiki CLI commands | `.claude/skills/gitnexus/gitnexus-cli/SKILL.md` |

<!-- gitnexus:end -->
