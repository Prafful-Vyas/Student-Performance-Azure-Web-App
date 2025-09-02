# End to End Azure Machine Learning Project

## Run from terminal:

Build the docker image
`docker build -t pvreg.azurecr.io/student_performance:latest .`

Login into your container registry
`docker login pvreg.azurecr.io`

push the image into the container registry
`docker push pvreg.azurecr.io/student_performance:latest`
