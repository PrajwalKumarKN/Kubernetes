Installation of kubectl on ubuntu :
# Get the latest stable version (corrected)
KUBECTL_VERSION=$(curl -sL https://dl.k8s.io/release/stable.txt)

# Download kubectl
curl -LO "https://dl.k8s.io/release/${KUBECTL_VERSION}/bin/linux/amd64/kubectl"

# Make it executable
chmod +x kubectl

# Move it to a directory in your PATH
sudo mv kubectl /usr/local/bin/

# Verify installation
kubectl version –client

Installation of Minikube on ubuntu :
1. Install dependencies
sudo apt-get update
sudo apt-get install -y curl wget apt-transport-https ca-certificates conntrack
________________________________________
2. Download the latest Minikube release
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
________________________________________
3. Install the binary
sudo install minikube-linux-amd64 /usr/local/bin/minikube
________________________________________
4. Verify installation
minikube version

Installation of Docker and gave permission :
Sudo apt install docker.io
Fix Docker Permissions
Run the following command to add your user to the Docker group:
sudo usermod -aG docker $USER
Then activate the new group in your current shell:
newgrp docker
Now try:
docker ps
✅ If it works without sudo, Docker is correctly configured.
Then start Minikube :
minikube start --driver=docker


