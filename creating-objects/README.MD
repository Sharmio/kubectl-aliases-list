### Creating Object 
```sh
alias k='kubectl'
alias kc='kubectl create'
alias kcf='kubectl create -f' 
export do="--dry-run=client -o yaml"    
```
```sh
# creating clusterrole
alias kccr='kubectl create clusterrole' #kubectl create clusterrole pod-reader --verb=get,list,watch --resource=pods
```
```sh
# creating clusterrolebinding

## Examples:
## Create a cluster role binding for user1, user2, and group1 using the cluster-admin cluster role
alias kccrb='kubectl create clusterrolebinding' 
## kubectl create clusterrolebinding cluster-admin --clusterrole=cluster-admin --user=user1 --user=user2 --group=group1
```
```sh
# creating configmap

## Examples:
## Create a new config map named my-config based on folder bar
alias kccm='kubectl create configmap' 
## kubectl create configmap my-config --from-file=path/to/bar
```
```sh
# creating cronjob

## Examples:
alias kccj='kubectl create cronjob'
## kubectl create cronjob my-job --image=busybox --schedule="*/1 * * * *"
## Create a cron job with a command
## kubectl create cronjob my-job --image=busybox --schedule="*/1 * * * *" -- date
```
```sh
# creating deploy or deployment

## Examples:
alias kcd='kubectl create deployment' or
alias kcd='kubectl create deploy'
## Create a deployment named my-dep that runs the busybox image
## kubectl create deployment my-dep --image=busybox

## Create a deployment with a command
## kubectl create deployment my-dep --image=busybox -- date

## Create a deployment named my-dep that runs the nginx image with 3 replicas
## kubectl create deployment my-dep --image=nginx --replicas=3

## Create a deployment named my-dep that runs the busybox image and expose port 5701
## kubectl create deployment my-dep --image=busybox --port=5701
```
