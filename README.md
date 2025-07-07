# HTMLDeploymentDocKube
docker run -d -p 3000:80 sowjanyajindam/webappimage 
minikube start
kubectl apply -f web-app-deployment.yaml
kubectl apply -f service.yaml
kubectl expose deployment my-webapp --type=NodePort --port=3000 --target-port=3000
kubectl port-forward service/webapp-service 3000:80
