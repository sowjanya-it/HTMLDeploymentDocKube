# HTMLDeploymentDocKube
<br> docker run -d -p 3000:80 sowjanyajindam/webappimage 
<br> minikube start
<br> kubectl apply -f web-app-deployment.yaml
<br> kubectl apply -f service.yaml
<br> kubectl expose deployment my-webapp --type=NodePort --port=3000 --target-port=3000
<br> kubectl port-forward service/webapp-service 3000:80
