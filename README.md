This project is a simple web application built using Node.js and Docker. The application allows users to enter their daily goals, check them off once completed, and remove them when done.

Features
- Enter daily goals
- Mark goals as completed
- Remove goals

Prerequisites
- Node.js
- Docker
- Docker Hub account

Getting Started
- Clone the Repository

git clone https://github.com/your-username/task-reminder-app.git
cd task-reminder-app

Dockerization
- Create a Dockerfile
I have already provided dockerfile in the repository. You can use that dockerfile. 

- Build the docker image
From the dockerfile you have to create a docker image by using command "docker build" with the required parameters. For the entire command, i have given the command below. In the below command "-t" specifies the name of the image. In my case i have given task-remainder-app for my image. You can use the same tag name or your desired tag name.

docker build -t task-remainder-app .

- Run the Docker Container
After creating the image, now you need to run the container by using "docker run" command, which helps you to create a container and run your image in the container. For the entire command, i have given the command below. Here in the below command you can see "-P' wich is port mapping, so this app will run only in the port 3000. I have also given this port mapping in the docker file too.

docker run -it -d -p 3000:3000 task-reaminder-app

After Running the above command, now you can see the web application in your browser and use it. 

Push the Docker Image to Docker Hub

1) Log in to Docker Hub:
docker login

2) Tag your Docker image:
docker tag task-reminder-app your-dockerhub-username/task-reminder-app:latest.

4) Push the image to Docker Hub:
docker push your-dockerhub-username/task-reminder-app:latest

Now your docker image is sent to the image registry that is docker hub.

- Deploying the Application
You can now deploy this Docker image on any container orchestration platform of your choice, such as Kubernetes, AWS ECS, or Docker Swarm.

Feel free to customize this template according to your project's specific details and requirements.

