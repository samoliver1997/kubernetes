##install kubectl

https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

1- curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

2- curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"

3- echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check

4- sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

##install minikube
https://minikube.sigs.k8s.io/docs/start/

1- curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
2- sudo install minikube-linux-amd64 /usr/local/bin/minikube
3- minikube start
