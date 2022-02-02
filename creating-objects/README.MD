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

```sh
# creating ingress

## Examples:
alias kci='kubectl create ingress'

## Create a single ingress called 'simple' that directs requests to foo.com/bar to svc
## svc1:8080 with a tls secret "my-cert"
##  kubectl create ingress simple --rule="foo.com/bar=svc1:8080,tls=my-cert"

## Create a catch all ingress of "/path" pointing to service svc:port and Ingress Class as "otheringress"
##  kubectl create ingress catch-all --class=otheringress --rule="/path=svc:port"
  
  # Create an ingress with two annotations: ingress.annotation1 and ingress.annotations2
  kubectl create ingress annotated --class=default --rule="foo.com/bar=svc:port" \
  --annotation ingress.annotation1=foo \
  --annotation ingress.annotation2=bla
  
  # Create an ingress with the same host and multiple paths
  kubectl create ingress multipath --class=default \
  --rule="foo.com/=svc:port" \
  --rule="foo.com/admin/=svcadmin:portadmin"
```
