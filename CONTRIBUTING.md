# Contributing to Zhivex

Thank you for helping improve Zhivex.

## Before opening a change

1. Search existing issues, pull requests, and discussions.
2. Use a discussion for support questions or early design proposals.
3. Use an issue for a reproducible bug or a scoped feature request.
4. Never include API keys, private prompts, customer data, or credentials.

## Pull requests

- Keep the change focused and explain the user impact.
- Add or update tests for observable behavior.
- Update public documentation and examples when usage changes.
- Record compatibility, security, and release implications.
- Run the validation commands documented by the target repository.
- Do not publish packages locally; releases run through protected GitHub
  workflows with trusted publishing.

For TypeScript projects, use Bun:

```bash
bun install
bun run typecheck
bun run test
bun run build
```

For Python projects, use the repository's Makefile:

```bash
make check
```

## Reviews

Maintainers may ask for a smaller scope, additional tests, migration guidance,
or security review. All required checks and review conversations must be
resolved before merge.

By participating, you agree to follow the
[Code of Conduct](./CODE_OF_CONDUCT.md).

