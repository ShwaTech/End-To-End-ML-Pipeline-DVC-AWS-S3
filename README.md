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

## Expermients with DVC ->

- pip install dvclive
- Add the dvclive code block (mentioned below)
- Do **"dvc exp run"**, it will create a new dvc.yaml(if already not there) and dvclive directory (each run will be considered as an experiment by DVC)
- Do **"dvc exp show"** on terminal to see the experiments or use extension on VSCode (install dvc extension)
- Note that DVC Vscode Extension Is Making Greatness 🔥 - The Process Easy
- Do **"dvc exp remove {exp-name}"** to remove exp (optional) | **"dvc exp apply {exp-name}"** to reproduce prev exp
- Change params, re-run code (produce new experiments)
- Now git add, commit, push

## Adding a remote S3 Storage To DVC ->

- Login to AWS Console
- Create an IAM User (Straight Forward Process)
- Attach Policies to the User -> AdministratorAccess , Then Create Access Key ID and Secret Access Key
- Create an S3 Bucket (Enter Unique Name and Create)
- pip install dvc[s3]
- pip install awscli
- aws configure
- dvc remote add -d dvcstore s3://bucket-name
- dvc commit, dvc push the exp output that we want to save
- Finally git add, commit, push

### Do Not Forget To Delete The IAM User and S3 Bucket When You Are Done With The Project Not To Cost You
