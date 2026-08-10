# Contributing

Default contribution guide for repositories in the `DashinDesign` organization. A project
that ships its own `CONTRIBUTING.md` overrides this one — read that instead.

This file covers what is true **across** projects. Stack-specific commands (how to
install, build, lint, and test) live in the individual repository's README or its own
contributing guide.

## Developer Certificate of Origin (DCO)

Every commit must be **signed off**. By signing off you certify — per the
[DCO](https://developercertificate.org/) — that you have the right to contribute the code
under the repository's licence.

Append `--signoff` (or `-s`) to every commit:

```sh
git commit -s -m "feat(parser): accept relative sitemap URLs"
```

This adds a trailer:

```
Signed-off-by: Your Name <your.email@example.com>
```

The name and email must match your `git config user.name` and `user.email`. To stop
thinking about the flag:

```sh
git config --global format.signoff true
```

Forgot to sign off? Amend the last commit with `git commit --amend --signoff`, or for a
whole branch: `git rebase --signoff <base>`.

## Commit messages

[Conventional Commits](https://www.conventionalcommits.org/):
`feat:`, `fix:`, `chore:`, `refactor:`, `docs:`, `test:`, `perf:`, `ci:`, `build:`,
`revert:`. Most repositories enforce this with a `commit-msg` hook and in CI.

## Workflow

1. Open an issue first for anything non-trivial. It's cheaper to disagree about the
   approach before the code exists.
2. Fork, then branch from the repository's development branch — not from a release branch.
3. Keep the pull request focused. One concern per PR; unrelated cleanups belong in their
   own.
4. Run the repository's full check command locally before pushing. CI is confirmation, not
   a search tool.

## Tests

- **Every bug fix ships a regression test.** Write it first, watch it fail for the right
  reason, then fix.
- A test that passes both with and without your fix is not catching anything. Restructure
  it or drop it.
- Tests exist to catch bugs, not to move a coverage number.

## Documentation

Documentation follows [Diátaxis](https://diataxis.fr/). A document is exactly one of
tutorial, how-to guide, reference, or explanation — mixed-type documents are the main
source of duplication. Put new docs in the matching quadrant.

Every fact has one canonical home. Other documents link to it; they do not restate it.

## Architectural decisions

Non-trivial architectural changes get an ADR (numbered, in `docs/adr/`). Changing a
previous decision means updating its ADR, not silently diverging from it.

## Licensing

Licensing is per-repository — read the `LICENSE` file before you start. Projects here are
not uniformly licensed: some are permissive, some copyleft. If a contribution's licensing
implications are unclear, ask in an issue first.

## Code of Conduct

Participation is governed by [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md).
