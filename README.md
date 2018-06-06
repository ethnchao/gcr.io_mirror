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

Total of 4's gcr.io/tf-on-k8s-dogfood/* images

-------


[gcr.io/tf-on-k8s-dogfood/gke-datalab √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.gke-datalab/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_operator √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_operator/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_operator-gpu-load √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_operator-gpu-load/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_sample √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_sample/tags/)

[gcr.io/tf-on-k8s-dogfood/tf_sample_gpu √](https://hub.docker.com/r/anjia0532/tf-on-k8s-dogfood.tf_sample_gpu/tags/)

