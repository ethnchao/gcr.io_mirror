Google Container Registry Mirror [last sync 2018-06-05 12:28 UTC]
-------

[![Sync Status](https://travis-ci.org/anjia0532/gcr.io_mirror.svg?branch=sync)](https://travis-ci.org/anjia0532/gcr.io_mirror)

Syntax
-------

```bash
gcr.io/namespace/image_name:image_tag eq anjia0532/namespace.image_name:image_tag
```

Example
-------

```bash
docker pull gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1 
# eq 
docker pull anjia0532/google-containers.federation-controller-manager-arm64:v1.3.1-beta.1
```

ReTag anjia0532 images to gcr.io 
-------

```bash
# replace gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1 to real image
# this will convert gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1 
# to anjia0532/google-containers.federation-controller-manager-arm64:v1.3.1-beta.1 and pull 
eval $(echo $(cat <<EOF
gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1
gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1
gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1
EOF
)| sed 's/gcr\.io/anjia0532/g;s/\//\./g;s/ /\n/g;s/anjia0532\./anjia0532\//g' | uniq | awk '{print "docker pull "$1";"}')

# this code will retag all of anjia0532's image from local  e.g. anjia0532/google-containers.federation-controller-manager-arm64:v1.3.1-beta.1 
# to gcr.io/google-containers/federation-controller-manager-arm64:v1.3.1-beta.1
eval $(docker images | grep anjia0532 | awk '{print $1":"$2}' |awk -F'[/.:]' '{printf "docker tag %s/%s.%s:%s gcr.io/%s/%s:%s;\n",$1,$2,$3,$4,$2,$3,$4}')
```

[Changelog](./CHANGES.md)
-------

Total of 6's gcr.io/k8s-minikube/* images

-------


[gcr.io/k8s-minikube/e2e √](https://hub.docker.com/r/anjia0532/k8s-minikube.e2e/tags/)

[gcr.io/k8s-minikube/localkube-dind-image √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-dind-image/tags/)

[gcr.io/k8s-minikube/localkube-dind-image-devshell √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-dind-image-devshell/tags/)

[gcr.io/k8s-minikube/localkube-image √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-image/tags/)

[gcr.io/k8s-minikube/nginx-ingress-controller √](https://hub.docker.com/r/anjia0532/k8s-minikube.nginx-ingress-controller/tags/)

[gcr.io/k8s-minikube/storage-provisioner √](https://hub.docker.com/r/anjia0532/k8s-minikube.storage-provisioner/tags/)

[gcr.io/k8s-minikube/tensorflow_grpc √](https://hub.docker.com/r/anjia0532/k8s-minikube.tensorflow_grpc/tags/)

