gcloud builds submit --tag []/my-spleeter-image . 
gcloud builds submit --config cloudbuild.yaml . # enables layer cache, speeds up docker image building

