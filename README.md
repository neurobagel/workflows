# workflows

This repo helps automatically synchronize shared workflows across repos.

`template_workflows/` and `template_configs/` contain inert templates for files we want in multiple repos - these templates are not doing anything on their own.

`.github/sync.yml` is a config file (containing repo names) which is read by `.github/workflows/sync_wf.yml`.

`.github/workflows/sync_wf.yml` is the actual unique active workflow in this repo which takes the files in the template directories and makes PRs to adds them to appropriate repos listed in the config file.
