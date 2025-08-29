flask hello-world project

Build and deploy a simple flask application using jenkins and K8s

# Prerequisties

* Python
* Flask
* Docker
* Git and GitHub
* Jenkins
* K8s

# Steps in the CI/CD pipeline

1. Create a "Hello world" Flask application
2. Dockerize the application
3. Create a github repository and push code to it
4. Test the code locally by building docker image and running it
5. Start Jenkins server on a host
6. Using ngrok to get ip for Jenkins and use webhook trigger with github
7. Write Jenkins pipeline to build and push the docker image to Docker
8. Set up K8s on a host using Minikube
9. Create a K8s deployment and service for the application
10. Use Jenkins to deploy the application on K8s

# Project structure

* app.py - Flask application which will print "Hello World" when you run it
* requirements.txt - Contains dependencies for the project
* Dockerfile - Contains commands to build and run the docker image
* Jenkinsfile - contains the pipeline script for build , push and deploy
* flask.yaml - K8s deployment and service file for the application
* flask-secret.yaml - K8s secret file
* flask-configmap.yaml - K8s configmap file
* postgres.yaml - K8s deployment and service file for postgres DB

# Conclusion

* In this project, I build a very simple CI/CD pipeline using Jenkins and K8s, don't forget to use ngrok in terminal and keep the terminal open so you can use the webhook
* I used credentials for docker hub and K8s, after deploy the application, run "minikube service flask-service" to access it in browser
