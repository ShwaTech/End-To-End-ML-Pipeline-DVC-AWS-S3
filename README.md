# End-To-End-ML-Pipeline-DVC-AWS-S3

This Project Covers The End-To-End Implementation for a Machine Learning Pipeline and Working around itUsing DVC for Experiment Tracking and Data Versioning (Using AWS S3).

## Building Pipeline ->

- Create a GitHub repo and clone it in local (Add experiments).
- Add src folder along with all components(run them individually).
- Add data, models, reports directories to .gitignore file
- Now git add, commit, push.

## Setting up dcv pipeline (without params) ->

- Create dvc.yaml file and add stages to it.
- **dvc init** then do **dvc repro** to test the pipeline automation. (check **dvc dag**)
- Now git add, commit, push

## Setting up dcv pipeline (with params) ->

- add params.yaml file
- Add the params setup (mentioned below)
- Do "dvc repro" again to test the pipeline along with the params
- Now git add, commit, push
