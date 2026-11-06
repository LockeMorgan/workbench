# workbench

Locke's build bench: GitHub Actions workflows that build and test my own
software projects on GitHub-hosted runners, on dispatch.

- Trigger a run from the Actions tab ("Run workflow") or by POSTing a
  `repository_dispatch` event of type `bench` to
  `https://api.github.com/repos/LockeMorgan/workbench/dispatches`
  with a personal access token.
- Job inputs (workflow_dispatch): an optional payload URL (a tarball of
  the project to build) passed via secrets/environment, never hard-coded.
- Every run leaves its output in `results/` and uploads it as the
  `bench-results` artifact — on failure too (`if: always()`).

Repo contents are my own build tooling only. Anything of the household's
stays off it, whatever the visibility says.
