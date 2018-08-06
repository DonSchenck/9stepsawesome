Test it plain
node -v
v8.11.3
npm -v
v8.11.3


node app.js
curl localhost:8000

Test it in Docker
minishift docker-env
minikube docker-env

docker build -t 9stepsawesome/mynode:v1 . 

docker images | grep mynode

docker run -d -p 8000:8000 9stepsawesome/mynode:v1

docker ps | grep mynode

docker stop 08efa083696b

docker rm 08efa083696b

deploy it into minikube/minishift
kubectl create -f kubefiles/mynode-deployment.yml