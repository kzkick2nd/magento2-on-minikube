$ minikube start --vm-driver=hyperkit
$ minikube dashboard

# Create Deployment
$ kubectl create deployment hello-node --image=gcr.io/hello-minikube-zero-install/hello-node
$ kubectl get deployments
$ kubectl get pods
$ kubectl get events
$ kubectl config view

# Create Service
$ kubectl expose deployment hello-node --type=LoadBalancer --port=8080
$ kubectl get services
$ minikube service hello-node # LB services を local オープンする

# Enable Addon
$ minikube addons list
$ minikube addons enable heapster
$ kubectl get pod,svc -n kube-system
$ minikube addons disable heapster

# Cleanup
$ kubectl delete service hello-node
$ kubectl delete deployment hello-node