## Steps for creating a docker image for our app

After creating the docker file 

create an image 
docker build -t scapp:v1.0.0 .

create a container of the image to test our app is reachable/working
docker run -d -p 80:80 scapp:v1.0.0
We are mapping the host port 80 to the container's port 80, so we can reach the service outside the container

Go to your browser: test the URL= http://localhost:80/index.html


Back to your terminal, tag the image and get it ready to push to docker registry/hub
docker tag scapp:v2.0.0 <docker id/username>/scapp:v1.0.0 

docker push <docker id/username>/scapp:v1.0.0 