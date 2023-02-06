# DE-Zoomcamp_Week-2 Homework Prefect-GitHub deployment
Deploying ETL pipeline in Prefect from GitHub repository.

## Steps to run prefect flow directly from this github repository:

* **Step 1:** Upload deployment repository to github (https://github.com/Mahdi-Moosa/DE-Zoomcamp_Week-2-HW_Prefect_GitHub-deployment).
* **Step 2:** run command: prefect deployment build etl_web_to_gcs.py:etl_parent_flow -sb github/github-hw-2-de-zoomcamp -n github_deployment_parent_flow -a

  *Note: The deployment build command needs local python file (apparenly to perfrom an intial check to generat the deployment yaml file).*
* **Step 3:** run command: prefect deployment apply etl_parent_flow-deployment.yaml
* **Step 4:** run command: prefect agent start --work-queue "default"

## Relevant resource:
* Blogpost link: https://mahdimoosa.substack.com/p/deploying-prefect-data-pipeline-directly

