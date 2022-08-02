[![CircleCI](https://dl.circleci.com/status-badge/img/gh/nonsosky/ML-Microservices-Project-4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/nonsosky/ML-Microservices-Project-4/tree/main)


<h3> Summary of the project </h3>
This repository contains code to containerize a Python machine learning application. The application uses a pre-trained sklearn model to forecast housing prices in Boston based on a variety of features, including the average number of rooms in a home and information on highway access, teacher-to-student ratios, and other factors. On the website for the data source, you can read more about the data, which was originally taken from <a href="https://www.kaggle.com/c/boston-housing">Kaggle</a>.
<br><br>
app.py serves out predictions about housing prices through API calls. This code could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.
<br><br>
The following contains instructions for running the app with Kubernetes or Docker.

<h3> Setup the Environment </h3>
<h5> Create a virtualenv and activate it </h5>
<ul>
  <li> python3 -m venv ~/.devops </li>
  <li> source ~/.devops/bin/activate </li>
  <li> Run `make install` to install the necessary dependencies </li>
</ul>

<h3> Instructions on how to run the Python scripts and web app </h3>
<ol>
  <li> Standalone:  `python app.py` </li>
  <li> Run in Docker:  `./run_docker.sh` </li>
  <li> Run in Kubernetes:  `./run_kubernetes.sh` </li>
</ol>

<h3> Kubernetes Steps </h3>
<ul>
  <li> Setup and Configure Docker locally </li>
  <li> Setup and Configure Kubernetes locally </li>
  <li> Create a Flask app in a Container </li>
  <li> Run via kubectl </li> 
  <li> You can choose to run one cluster locally with [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/) </li>
</ul>

<h3>Dockerfile</h3>
It is a text-based script containing instructions that is used to create a Docker container image

<h3>Makefile</h3>
The Makefile script is a file that contains a set of directives used to build the app

<h3> app.py </h3>
serves out predictions about housing prices through API calls

<h3> make_prediction.sh </h3>
This shell script is responsible for sending some input data to your containerized application via the appropriate port

<h3> run_docker.sh </h3>
This shell script is responsible for building the container docker image

<h3> upload_docker.sh </h3>
This shell script is responsible for uploading an image to dockerhub

<h3> run_kubernetes.sh </h3>
This script is responsible for deploying the application

<h3> model_data </h3>
The model_data directory is housing 'boston_housing_prediction.joblib' and 'housing.csv' which are files containing the Machinne Learning trained data used for the application

<h3> output_txt_files </h3>
The output_txt_files directory is housing 'docker_out.txt' and 'kubernetes_out.txt' which are files containing the Docker and Kubernetes output logs respectively.

<h3> .circleci </h3>
The .circleci directory is hosing 'config.yml' file which is used to test your repository with CircleCI 
