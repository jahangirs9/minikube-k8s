# minikube-k8s

first we need to Launch EC2 in there select t2-medium and volume must be 20gb
cd /usr/local/bin ( chance the directory)
sudo su
sudo apt update
sudo apt update && apt -y install docker.io
curl -LO "https://storage.googleapis.com/kubernetes-release/release/v1.21.0/bin/linux/amd64/kubectl"
chmod +x ./kubectl
curl -LO "https://github.com/kubernetes/minikube/releases/download/v1.22.0/minikube-linux-amd64"
chmod +x minikube-linux-amd64
sudo mv minikube-linux-amd64 /usr/local/bin/minikube
apt install conntrack
minikube start --vm-driver=none (if not worked then use next)
minikube start --driver=docker --force
minikue status
