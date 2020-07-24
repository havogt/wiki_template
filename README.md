# Track changes in your Wiki with PRs

GitHub manages the wiki in a separate repository at `https://github.com/<github_user>/<repo_name>.wiki.git`,
e.g. `https://github.com/havogt/wiki_template.wiki.git` for this repository. The wiki doesn't natively support
editing the wiki via PRs and therefore doesn't allow reviewing and commenting on changes.
This workflow works around this limitation.

## Features

- Edit wiki pages with PRs to the main repository.
- Open PRs automatically if a Wiki page is edit from the UI.

## How does it work?

The content of the wiki is copied to the main repository and declared as upstream (from now on it is the single source of truth),
while the wiki repository is now only a mirror.
The mirror is kept up-to-date by a GitHub action.

Additionally all changes (accidentally or not) via the UI of the wiki are reverted and opened as PRs for review.

## How to manage Wikis of code repositories

In the workflow described above the sole purpose of the repository is a to keep the wiki. In case you want to manage the wiki in a repository which contains code,
the workflow can be easily adapted to keep the wiki in a dedicated `wiki` branch.

## Feedback

Please open issues for feedback to this workflow.
