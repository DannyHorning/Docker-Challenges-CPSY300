# Docker Challenge
## Danny Horning
### 000702974

## What is Docker?
Docker is a platform that is designed to help developers make, deploy, and run applications using containers. Containers are essentially a package that pack up all the necessary packages and dependencies that an 
application requires to run. This way, a program is not dependent on the system of the user, because the package contains all of the necessary dependencies. For example, if I create a project using Node 14, but the
user that I am trying to deliver the project to only has Node 9, this won't matter, because the container that has been deployed has all of the packages and dependencies of Node 14. This greatly reduces the
"Well it works on my machine!" scenario from happening.

## Installing Docker
Ubuntu is required for Docker, so running the command wsl --install in powershell. Make sure that your virtualization settings are on (you can do this from the BIOS, this link help me: https://support.salad.com/article/281-enable-virtualization-by-motherboard-gigabyte). Then you can install Docker Desktop, and you should be good to start making your containers (just make sure that Docker Desktop is running, or you will get some funky errors).

**Challenge 1**
The challenge was to write an HTML program, and place this file in a docker container so the container could be hosted on a local server.
I was mostly learning how to write a Dockerfile, which went building, directs Docker on how to build the application. Some of the common commands used in the process were docker build -t, and docker run

**Challenge 2**
The second challenge was to take a Node.js, and use docker-compose to be able to host the server and have it communicate with an API. This one was a lot trickier, and took a lot of googling for answers (see the reference list). The docker file worked generally the same, with a couple of new lines for me. The most confusing one was the EXPOSE line, but eventually I learned that this was just to talk to the node server. The 
docker-compose file was also new to me, but was fairly straight forward in giving directions on how the container and api would talk. Lastly, I had to override the NGinx file to listen to the container port 80, and proxy any request to the port 3000. The build process was only composed of docker-compose up --build. This built the server and hosted it on the localhost.

One of the biggest problems I had with this project, was trying to install docker. From the BIOS I had to look for VM settings, which was blocking the clean installation of Ubuntu. Once I changed my VM settings in the BIOS start up, I was able to reinstall and get Docker Desktop set up

### See the PDF files to look at the step by step process and references
