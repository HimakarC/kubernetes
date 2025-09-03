## To Create a Load Serive type....

**<u>Step-1</u>:** Create an EKS Cluster with **eksctl** <br>
--> **eksctl** provisions the entire EKS stack: **VPC, subnets, security groups, IAM roles, EC2 worker nodes and control plane. <br>

**<u>Step-2</u>:** Associate IAM OIDC Provider <br>
--> EKS uses IAM Roles for service Accounts (IRSA) to securely grant permissions to K8s pods. <br>
--> This step enables your cluster to trust an OIDC identity provider, which is required for the AWS Load Balancer Controller to assume its IAM role. <br>

**<u>Step-3</u>:** Create IAM Policy for Load Balancer Controller <br>
--> The controller needs permissions to create and manage AWS resources like ALBs, Target Groups, Security Groups, etc. <br>
--> This policy defines those permissions and is attached to the service account in the next step. <br>

**<u>Step-4</u>:** Create IAM Service Account via **eksctl** <br>
--> This creates a Kubernetes service account in the kube-system namespace and links it to the IAM policy. <br>
--> The AWS Load Balancer Controller will use this account to interact with AWS APIs securely. <br>

**<u>Step-5</u>:** Install AWS Load Balancer Controller via Helm <br>
--> This installs the controller that translates Kubernetes Service and Ingress resources into AWS ALBs/NLBs.
