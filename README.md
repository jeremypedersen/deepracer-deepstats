- **Last Updated:** 2024-09-02
- **Last Tested:** PENDING

# DeepRacer DeepStats

Welcome! The code here consists of:

1. A CloudFormation `.yaml` file to set up a SageMaker Notebook environment
2. Some `.ipynb` files (Jupyter Notebooks) which can help you analyze DeepRacer training and evaluation data, and find ways to improve your models

The notebooks here borrow heavily from existing code you can find online. In particular:

1. The [DeepRacer community log analysis code](https://github.com/aws-deepracer-community/deepracer-analysis)  
1. The [AWS DeepRacer 400L workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/66473261-de66-42a1-b280-3e0ec87aee26/en-US/account-access)

Happy Racing! 

## A quick note on the repository's contents

All of the staging and temporary files created while unpacking logs and models have been committed alongside the Jupyter Notebook file, so you can see what happens after a successful run of the notebook. 

## Testing the code

Example models, evaluation logs, and training logs are located in `local_model_files`. Comment out the relevant code under **Fetch Logs and (Optionally) DeepRacer Model Checkpoint** in `DeepRacer Log Analysis.ipynb` to try them out! 

Currently, the code has been tested and found to work for:

- PPO model training jobs, downloaded from DeepRacer directly via the AWS API (both continuous and discrete action spaces)
- PPO model evaluation jobs, downloaded from DeepRacer directly via the AWS API (both continuous and discrete action spaces)
- PPO model training data, locally in `local_model_files` (both continuous and discrete action spaces)
- PPO model evaluation data, locally in `local_model_files` (both continuous and discrete action spaces)

If you want to run the code on your own models, either: 

1. Install and configure the AWS CLI and create an Access Key linked to an IAM user with permissions to use the DeepRacer services

or 

2. Download your model file (via "Actions -> Download Physical Car Model") and training or evaluation logs (via the "Download logs" button, save them in `local_model_files` and update the relevant paths under **Fetch Logs and (Optionally) DeepRacer Model Checkpoint** in `DeepRacer Log Analysis.ipynb`

That's it! 

