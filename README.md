To clone this repo, use command as - git clone https://github.com/bhaskarmehta/BookStoreBackend.git


After clonning this, we need to create a .env file and store two variable, if we want to run this in local
 1) PORT 2) DBConnection

We have created a Dockerfile and ci pipeline. Thus pipeline will trigger when a new changes is pushed to this master branch. It will create a new Docker image and push it to the dockerhub.
In secret, we have to store the Docker hub credential like docker hub username as DOCKERHUB_ID and docker password or token as DOCKERHUB_PASSWORD

Now if we want to use or run this docker image then we have to run the docker command as-

docker run -d -p 3000:3000 -e PORT=3000 -e DBConnection="Connection url ex- mongodb://12.230.12.34:27017" <image name>
