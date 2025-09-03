## To Create a cluster using eksctl <br>
--> eksctl create cluster --name=<your-cluster-name> --region=<your-region>  --fargate <br>

### To Implement a LoadBalancer Service in Kubernetes on a cloud platform like AWS, you need to ensure your cluster is configured to integrate with the cloud provider’s native load balancer. <br>
### To use Amazon EKS Cluster <br>

--> Firstly, Install AWS CLI and configure the credentials of AWS Account <br>
## Now, Connect to the EKS Cluster <br>
--> aws eks --region <region> update-kubeconfig --name <cluster-name> <br>
--> kubectl get nodes #You will see worker nodes (EC2 Instances) <br>

## Now, Create services and expose the application and run.
