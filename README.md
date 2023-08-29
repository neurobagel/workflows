# workflows

This repo helps automatically synchronize shared workflows across repos.

`workflows/` contains inert templates for workflows we want in multiple repos - these templates are not doing anything on their own.

`.github/sync.yml` is a config file (containing repo names) which is read by `.github/workflows/sync_wf.yml`.

`.github/workflows/sync_wf.yml` is the actual unique active workflow in this repo which takes everything in `workflows/` and makes PRs to add them to each repo listed in the config file.
