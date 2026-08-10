# `.github`

Organization-wide defaults for the [`DashinDesign`](https://github.com/DashinDesign) org.

Files here are **fallbacks**. Any repository that ships its own copy of a file overrides
the default — nothing in this repo can force a policy onto a repo that has its own.

| File | Applies to |
| --- | --- |
| `profile/README.md` | the org profile page at github.com/DashinDesign |
| `CODE_OF_CONDUCT.md` | every org repo without its own |
| `CONTRIBUTING.md` | every org repo without its own |
| `SECURITY.md` | every org repo without its own |
| `SUPPORT.md` | every org repo without its own |
| `.github/FUNDING.yml` | every org repo without its own |
| `.github/ISSUE_TEMPLATE/` | every org repo without its own |
| `.github/pull_request_template.md` | every org repo without its own |

Two things that are **not** possible here, by GitHub's design:

- **`LICENSE` cannot be defaulted.** Every repo needs its own, so the licence travels
  with the code when it is cloned, packaged, or downloaded.
- **This repo must stay public.** Private `.github` repositories are not supported, and
  issue/PR template defaults in particular require public visibility.

Reference: <https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file>
