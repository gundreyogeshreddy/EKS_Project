I deployed a 2048 game application using Kubernetes on AWS Elastic Kubernetes Service (EKS) platform.

* Below is the procedure that i followed;

➡ Created a EKS cluster with Fargate.

➡ Created Fargate profile on EKS cluster.

➡ Created a deployment, service, ingress resource.

➡ Set up an IAM OIDC provider with EKS cluster which will enable it to use IAM roles for service account.

➡ Created a iam policy, iam service account and attached the iam policy, where it can be communicate to the AWS service.

➡ Now set up the ingress controller to automatically create an ALB controller.

➡ Deployed ALB controller by using helm charts and now we can see that AWS Load Balancer Controller installed.

➡Ingress Controller reads the configuration provided in the ingress resource based on the ingress rules, ingress controller creates and configures the Load Balancer.

➡Finally, through the application load balancer DNS address, we can get the request and we can access the 2048 game application with high availability and scalability ✓.
