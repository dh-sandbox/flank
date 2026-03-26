# Agents

## Code Quality

This project uses [Qlty CLI](https://qlty.sh) for code quality. Configuration is in `.qlty/qlty.toml`.

Before committing, ALWAYS run auto-formatting:

```sh
qlty fmt
```

Before pushing, ALWAYS run linting and fix any errors:

```sh
qlty check --fix --level=low
```

If issues remain that cannot be auto-fixed, resolve them manually before pushing.

## Repository Setup

After cloning, enable the shared git hooks:

```sh
git config core.hooksPath .githooks
```

This enforces `qlty fmt` on commit and `qlty check` on push.

## Kotlin Style

ktlint is the primary Kotlin linter. Style rules are defined in the root `.editorconfig`:

- 4-space indentation
- 120 character max line length
- Trailing commas required
- No blank lines at the start of class or method bodies
- Braces required on multiline if/else
