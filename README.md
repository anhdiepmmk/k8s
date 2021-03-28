## Configuring the AWS CLI
> https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html
```
aws configure
```
## Create a kubeconfig for Amazon EKS  
> https://docs.aws.amazon.com/eks/latest/userguide/create-kubeconfig.html
```
aws eks --region ap-southeast-1 update-kubeconfig --name kub-dep-demo
```
## Context manipulate
> Get contexts
```
kubectl config get-contexts
```
> Show which one is current context
```
kubectl config current-context
```
> Set current context by context name

```
kubectl config use-context my-cluster-name
```