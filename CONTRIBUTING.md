# Contributing to Devmentech repositories

Use this workflow unless the target repository documents a stricter one.
Repository-specific instructions always take precedence.

## Quick path

1. Read the repository `README.md`, `AGENTS.md`, and local contribution guide.
2. Confirm the work is approved or linked to an issue when the repository
   requires issue-first development.
3. Branch from the repository's documented integration branch.
4. Implement one reviewable work unit with its tests and documentation.
5. Open a pull request using the default template and wait for review.

## Working agreements

- Never push directly to a long-lived branch such as `main` or `develop`.
- Use the package manager, runtime, and commands declared by the repository.
- Keep generated files, lockfiles, migrations, and documentation with the
  change that requires them.
- Do not bypass tests, hooks, or required checks to make a change pass.
- Never commit credentials, tokens, private keys, customer data, or production
  configuration.
- Prefer the smallest change that completely solves the stated problem.

## Branches and commits

Use a short branch name in the form `type/description`, for example
`feat/user-invitations` or `fix/session-expiration`.

Commit messages follow Conventional Commits:

```text
<type>(<optional-scope>): <outcome>
```

Common types are `feat`, `fix`, `docs`, `refactor`, `test`, `build`, `ci`, and
`chore`. A commit should represent a working behavior, correction, migration,
or documentation unit, not an arbitrary group of file types.

## Pull requests

A pull request should:

- explain the problem and the resulting behavior;
- link the approved issue when the repository requires one;
- select exactly one change type;
- include verification commands and their results;
- disclose risks, migrations, rollout steps, and rollback boundaries;
- keep tests and user-facing documentation with the implementation;
- avoid unrelated cleanup.

Reviewers may ask for a large pull request to be split into independent work
units. The author remains responsible for responding to review feedback and
keeping the branch current.

## Security

Do not disclose a suspected vulnerability in a public issue, pull request, or
discussion. Follow [`SECURITY.md`](SECURITY.md) instead.
