Create Fargate profile :

eksctl create fargateprofile \
    --cluster demo-cluster \
    --region us-east-1 \
    --name alb-sample-app \
    --namespace game-2048
    

Deploy the deployment, service and Ingress :

kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml


Create IAM OIDC provider with below command :

eksctl utils associate-iam-oidc-provider --cluster demo-cluster --region <your-region> --approve # which will integrate the IAM OIDC provider
