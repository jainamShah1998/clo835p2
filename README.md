# clo835p2
Make sure to have the minikube installed
start the minikube
- minikube start

# Step 1: Clone the repository

# Step 2: Build the docker image

 docker build -t project2clo835 .

# Step 3: Tag and Push the Docker Image to your Git Hub Repo

docker tag project2clo835 jainamshah24/project2clo835:latest
docker push jainamshah24/project2clo835:latest

# Step 4: Create the docker network and run the docker within the network
docker network create project2clo
docker run --network project2clo --name python-app -dp 3030:3030 jainamshah24/project2clo835:latest

# Step 5: 
Service YAML file using NodePort to expose the application 

We need to deploy the Manifests to Kubernetes for this we need to run the following command:

minikube status

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

kubectl get pods


# Step 6: Now run the below command in Powershell with admin priviledges to know the IP:

minikube ip
copy the IP: http://172.28.50.87:30300
with this we get the output of current location and time.

