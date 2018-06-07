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

Total of 17's gcr.io/spinnaker-marketplace/* images
-------


[gcr.io/spinnaker-marketplace/backend √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.backend/tags/)

[gcr.io/spinnaker-marketplace/clouddriver √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.clouddriver/tags/)

[gcr.io/spinnaker-marketplace/deck √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.deck/tags/)

[gcr.io/spinnaker-marketplace/echo √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.echo/tags/)

[gcr.io/spinnaker-marketplace/fiat √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.fiat/tags/)

[gcr.io/spinnaker-marketplace/front50 √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.front50/tags/)

[gcr.io/spinnaker-marketplace/frontend √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.frontend/tags/)

[gcr.io/spinnaker-marketplace/gate √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.gate/tags/)

[gcr.io/spinnaker-marketplace/gradle_cache √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.gradle_cache/tags/)

[gcr.io/spinnaker-marketplace/halyard √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.halyard/tags/)

[gcr.io/spinnaker-marketplace/halyard √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.halyard/tags/)

[gcr.io/spinnaker-marketplace/igor √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.igor/tags/)

[gcr.io/spinnaker-marketplace/igor √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.igor/tags/)

[gcr.io/spinnaker-marketplace/kayenta √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.kayenta/tags/)

[gcr.io/spinnaker-marketplace/kayenta √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.kayenta/tags/)

[gcr.io/spinnaker-marketplace/monitoring-daemon √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.monitoring-daemon/tags/)

[gcr.io/spinnaker-marketplace/monitoring-daemon √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.monitoring-daemon/tags/)

[gcr.io/spinnaker-marketplace/orca √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.orca/tags/)

[gcr.io/spinnaker-marketplace/orca √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.orca/tags/)

[gcr.io/spinnaker-marketplace/rosco √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.rosco/tags/)

[gcr.io/spinnaker-marketplace/rosco √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.rosco/tags/)

[gcr.io/spinnaker-marketplace/spinbot √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinbot/tags/)

[gcr.io/spinnaker-marketplace/spinbot √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinbot/tags/)

[gcr.io/spinnaker-marketplace/spinnaker-monitoring √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinnaker-monitoring/tags/)

[gcr.io/spinnaker-marketplace/spinnaker-monitoring √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinnaker-monitoring/tags/)

[gcr.io/spinnaker-marketplace/spinnaker-monitoring-daemon √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinnaker-monitoring-daemon/tags/)

[gcr.io/spinnaker-marketplace/spinnaker-monitoring-daemon √](https://hub.docker.com/r/anjia0532/spinnaker-marketplace.spinnaker-monitoring-daemon/tags/)


Total of 6's gcr.io/k8s-minikube/* images
-------


[gcr.io/k8s-minikube/e2e √](https://hub.docker.com/r/anjia0532/k8s-minikube.e2e/tags/)

[gcr.io/k8s-minikube/localkube-dind-image √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-dind-image/tags/)

[gcr.io/k8s-minikube/localkube-dind-image-devshell √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-dind-image-devshell/tags/)

[gcr.io/k8s-minikube/localkube-image √](https://hub.docker.com/r/anjia0532/k8s-minikube.localkube-image/tags/)

[gcr.io/k8s-minikube/nginx-ingress-controller √](https://hub.docker.com/r/anjia0532/k8s-minikube.nginx-ingress-controller/tags/)

[gcr.io/k8s-minikube/storage-provisioner √](https://hub.docker.com/r/anjia0532/k8s-minikube.storage-provisioner/tags/)

[gcr.io/k8s-minikube/tensorflow_grpc √](https://hub.docker.com/r/anjia0532/k8s-minikube.tensorflow_grpc/tags/)



Total of 4's gcr.io/tf-on-k8s-dogfood/* images
-------


[gcr.io/tf-on-k8s-dogfood/gke-datalab √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.gke-datalab/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_operator √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_operator/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_operator-gpu-load √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_operator-gpu-load/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_sample √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_sample/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_sample_gpu √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_sample_gpu/tags/)


Total of 3's gcr.io/kubernetes-helm/* images
-------


[gcr.io/kubernetes-helm/expandybird √](https://hub.docker.com/r/anjia0532/kubernetes-helm.expandybird/tags/)

[gcr.io/kubernetes-helm/manager √](https://hub.docker.com/r/anjia0532/kubernetes-helm.manager/tags/)

[gcr.io/kubernetes-helm/resourcifier √](https://hub.docker.com/r/anjia0532/kubernetes-helm.resourcifier/tags/)

[gcr.io/kubernetes-helm/tiller √](https://hub.docker.com/r/anjia0532/kubernetes-helm.tiller/tags/)

