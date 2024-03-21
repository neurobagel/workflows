# workflows

This repo helps automatically synchronize shared workflows across repos.

`template_workflows/` and `template_configs/` contain inert templates for files we want in multiple repos - these templates are not doing anything on their own.
- `template_workflows/auto_release` handles release automation workflows for a limited set of repositories
- `template_workflows/project_automation` handles generic workflows for a large number of repositories
- `template_configs/` handles files that should be synced with the root of a repository

You can see the list of repositories that these directories are currently kept in sync with here: https://github.com/neurobagel/workflows/blob/main/.github/sync.yml

`.github/sync.yml` is a config file (containing repo names) which is read by `.github/workflows/sync_wf.yml`.

`.github/workflows/sync_wf.yml` is the actual unique active workflow in this repo which takes the files in the template directories and makes PRs to adds them to appropriate repos listed in the config file.
