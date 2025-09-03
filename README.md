To install **kubectl**, need to install **minikube**

To install **minikube**:
--> curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 <br>
--> sudo install minikube-linux-amd64 /usr/local/bin/minikube <br>

To install **kubectl**: <br>
--> sudo apt-get install -y apt-transport-https ca-certificates curl <br>
--> curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.28/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg <br>
--> echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.28/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list <br>
--> sudo apt-get install -y kubectl <br>

To install **eksctl**: <br>
--> curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
--> sudo mv /tmp/eksctl /usr/local/bin
