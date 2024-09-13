# GCP config
	gcloud init

	gcloud auth configure-docker

	gcloud builds submit --tag gcr.io/[]/my-spleeter-image . 

After the build:
You can verify this by checking the list of images in GCR:
	gcloud container images list --repository=[gcr.io/[PROJECT_ID]](http://gcr.io/%5BPROJECT_ID%5D)


	gcloud run deploy my-spleeter-service [params]

Then:
	gcloud builds submit --config cloudbuild.yaml . # enables layer cache, speeds up docker image building

Define env vars on GCP config:

then:
	bucket_name = os.getenv('BUCKET_NAME', 'default-bucket-name')
	stems_number = os.getenv('STEMS_NUMBER', '5')

