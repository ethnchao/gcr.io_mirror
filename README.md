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

Total of 445's gcr.io/google-containers/* images

-------


[gcr.io/google-containers/zookeeper-install-3.5.0-alpha √](https://hub.docker.com/r/anjia0532/google-containers.zookeeper-install-3.5.0-alpha/tags/)

[gcr.io/google-containers/zookeeper-install √](https://hub.docker.com/r/anjia0532/google-containers.zookeeper-install/tags/)

[gcr.io/google-containers/zeppelin-proxy √](https://hub.docker.com/r/anjia0532/google-containers.zeppelin-proxy/tags/)

[gcr.io/google-containers/zeppelin √](https://hub.docker.com/r/anjia0532/google-containers.zeppelin/tags/)

[gcr.io/google-containers/kube-cross √](https://hub.docker.com/r/anjia0532/google-containers.kube-cross/tags/)

[gcr.io/google-containers/kube-cross √](https://hub.docker.com/r/anjia0532/google-containers.kube-cross/tags/)

[gcr.io/google-containers/webhooks-publisher √](https://hub.docker.com/r/anjia0532/google-containers.webhooks-publisher/tags/)

[gcr.io/google-containers/vpa-updater √](https://hub.docker.com/r/anjia0532/google-containers.vpa-updater/tags/)

[gcr.io/google-containers/kubectl √](https://hub.docker.com/r/anjia0532/google-containers.kubectl/tags/)

[gcr.io/google-containers/kubectl √](https://hub.docker.com/r/anjia0532/google-containers.kubectl/tags/)

[gcr.io/google-containers/vpa-recommender √](https://hub.docker.com/r/anjia0532/google-containers.vpa-recommender/tags/)

[gcr.io/google-containers/vpa-admission-controller √](https://hub.docker.com/r/anjia0532/google-containers.vpa-admission-controller/tags/)

[gcr.io/google-containers/kubedash √](https://hub.docker.com/r/anjia0532/google-containers.kubedash/tags/)

[gcr.io/google-containers/kubedash √](https://hub.docker.com/r/anjia0532/google-containers.kubedash/tags/)

[gcr.io/google-containers/kube-discovery-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-amd64/tags/)

[gcr.io/google-containers/kube-discovery-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-amd64/tags/)

[gcr.io/google-containers/kube-discovery-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm/tags/)

[gcr.io/google-containers/kube-discovery-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm/tags/)

[gcr.io/google-containers/kube-discovery-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm64/tags/)

[gcr.io/google-containers/kube-discovery-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm64/tags/)

[gcr.io/google-containers/volume-rbd √](https://hub.docker.com/r/anjia0532/google-containers.volume-rbd/tags/)

[gcr.io/google-containers/kubedns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-amd64/tags/)

[gcr.io/google-containers/kubedns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-amd64/tags/)

[gcr.io/google-containers/volume-nfs √](https://hub.docker.com/r/anjia0532/google-containers.volume-nfs/tags/)

[gcr.io/google-containers/volume-iscsi √](https://hub.docker.com/r/anjia0532/google-containers.volume-iscsi/tags/)

[gcr.io/google-containers/kubedns-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm/tags/)

[gcr.io/google-containers/kubedns-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm/tags/)

[gcr.io/google-containers/volume-gluster √](https://hub.docker.com/r/anjia0532/google-containers.volume-gluster/tags/)

[gcr.io/google-containers/volume-csi √](https://hub.docker.com/r/anjia0532/google-containers.volume-csi/tags/)

[gcr.io/google-containers/volume-ceph √](https://hub.docker.com/r/anjia0532/google-containers.volume-ceph/tags/)

[gcr.io/google-containers/kubedns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm64/tags/)

[gcr.io/google-containers/kubedns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm64/tags/)

[gcr.io/google-containers/update-demo √](https://hub.docker.com/r/anjia0532/google-containers.update-demo/tags/)

[gcr.io/google-containers/kube-dnsmasq-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-amd64/tags/)

[gcr.io/google-containers/kube-dnsmasq-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-amd64/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm/tags/)

[gcr.io/google-containers/ubuntu-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-ppc64le/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm64/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm64/tags/)

[gcr.io/google-containers/kube-dnsmasq-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-ppc64le/tags/)

[gcr.io/google-containers/kube-dnsmasq-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-ppc64le/tags/)

[gcr.io/google-containers/ubuntu-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm64/tags/)

[gcr.io/google-containers/kube-dns-perf-client-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dns-perf-client-amd64/tags/)

[gcr.io/google-containers/kube-dns-perf-client-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dns-perf-client-amd64/tags/)

[gcr.io/google-containers/ubuntu-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm/tags/)

[gcr.io/google-containers/kubedns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-ppc64le/tags/)

[gcr.io/google-containers/kubedns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-ppc64le/tags/)

[gcr.io/google-containers/kube-haproxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-haproxy/tags/)

[gcr.io/google-containers/kube-haproxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-haproxy/tags/)

[gcr.io/google-containers/ubuntu-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-amd64/tags/)

[gcr.io/google-containers/ubuntu-slim √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim/tags/)

[gcr.io/google-containers/kube-keepalived-vip √](https://hub.docker.com/r/anjia0532/google-containers.kube-keepalived-vip/tags/)

[gcr.io/google-containers/kube-keepalived-vip √](https://hub.docker.com/r/anjia0532/google-containers.kube-keepalived-vip/tags/)

[gcr.io/google-containers/ubuntu-nvidia-driver-installer √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-nvidia-driver-installer/tags/)

[gcr.io/google-containers/ubuntu √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu/tags/)

[gcr.io/google-containers/toolbox √](https://hub.docker.com/r/anjia0532/google-containers.toolbox/tags/)

[gcr.io/google-containers/tiny-glibc-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-ppc64le/tags/)

[gcr.io/google-containers/tiny-glibc-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm64/tags/)

[gcr.io/google-containers/tiny-glibc-arm √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm/tags/)

[gcr.io/google-containers/tiny-glibc-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-amd64/tags/)

[gcr.io/google-containers/tf-models √](https://hub.docker.com/r/anjia0532/google-containers.tf-models/tags/)

[gcr.io/google-containers/test-webserver √](https://hub.docker.com/r/anjia0532/google-containers.test-webserver/tags/)

[gcr.io/google-containers/test_subdir_1 √](https://hub.docker.com/r/anjia0532/google-containers.test_subdir_1/tags/)

[gcr.io/google-containers/kubekins-e2e √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-e2e/tags/)

[gcr.io/google-containers/kubekins-e2e √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-e2e/tags/)

[gcr.io/google-containers/tensorflow-gpu-notebook √](https://hub.docker.com/r/anjia0532/google-containers.tensorflow-gpu-notebook/tags/)

[gcr.io/google-containers/kubekins-job-builder √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-job-builder/tags/)

[gcr.io/google-containers/kubekins-job-builder √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-job-builder/tags/)

[gcr.io/google-containers/kubekins-test √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-test/tags/)

[gcr.io/google-containers/kubekins-test √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-test/tags/)

[gcr.io/google-containers/kubelet-to-gcm √](https://hub.docker.com/r/anjia0532/google-containers.kubelet-to-gcm/tags/)

[gcr.io/google-containers/kubelet-to-gcm √](https://hub.docker.com/r/anjia0532/google-containers.kubelet-to-gcm/tags/)

[gcr.io/google-containers/kube-nethealth-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-nethealth-amd64/tags/)

[gcr.io/google-containers/kube-nethealth-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-nethealth-amd64/tags/)

[gcr.io/google-containers/submit-queue √](https://hub.docker.com/r/anjia0532/google-containers.submit-queue/tags/)

[gcr.io/google-containers/stress √](https://hub.docker.com/r/anjia0532/google-containers.stress/tags/)

[gcr.io/google-containers/startup-script √](https://hub.docker.com/r/anjia0532/google-containers.startup-script/tags/)

[gcr.io/google-containers/spartakus-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.spartakus-amd64/tags/)

[gcr.io/google-containers/spark-worker √](https://hub.docker.com/r/anjia0532/google-containers.spark-worker/tags/)

[gcr.io/google-containers/spark-master √](https://hub.docker.com/r/anjia0532/google-containers.spark-master/tags/)

[gcr.io/google-containers/spark-driver √](https://hub.docker.com/r/anjia0532/google-containers.spark-driver/tags/)

[gcr.io/google-containers/spark-base √](https://hub.docker.com/r/anjia0532/google-containers.spark-base/tags/)

[gcr.io/google-containers/spark √](https://hub.docker.com/r/anjia0532/google-containers.spark/tags/)

[gcr.io/google-containers/slo-monitor √](https://hub.docker.com/r/anjia0532/google-containers.slo-monitor/tags/)

[gcr.io/google-containers/skydns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.skydns-ppc64le/tags/)

[gcr.io/google-containers/skydns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm64/tags/)

[gcr.io/google-containers/skydns-arm √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm/tags/)

[gcr.io/google-containers/skydns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-amd64/tags/)

[gcr.io/google-containers/skydns √](https://hub.docker.com/r/anjia0532/google-containers.skydns/tags/)

[gcr.io/google-containers/shyamjvs-prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-prometheus-to-sd/tags/)

[gcr.io/google-containers/shyamjvs-logexp √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-logexp/tags/)

[gcr.io/google-containers/shame-mailer √](https://hub.docker.com/r/anjia0532/google-containers.shame-mailer/tags/)

[gcr.io/google-containers/servicelb √](https://hub.docker.com/r/anjia0532/google-containers.servicelb/tags/)

[gcr.io/google-containers/serve-hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-s390x/tags/)

[gcr.io/google-containers/serve_hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-s390x/tags/)

[gcr.io/google-containers/serve-hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-ppc64le/tags/)

[gcr.io/google-containers/serve_hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-ppc64le/tags/)

[gcr.io/google-containers/serve-hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm64/tags/)

[gcr.io/google-containers/serve_hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm64/tags/)

[gcr.io/google-containers/serve-hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm/tags/)

[gcr.io/google-containers/serve_hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm/tags/)

[gcr.io/google-containers/serve-hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-amd64/tags/)

[gcr.io/google-containers/serve_hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-amd64/tags/)

[gcr.io/google-containers/serve_hostname √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname/tags/)

[gcr.io/google-containers/sd-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.sd-dummy-exporter/tags/)

[gcr.io/google-containers/rethinkdb √](https://hub.docker.com/r/anjia0532/google-containers.rethinkdb/tags/)

[gcr.io/google-containers/resource_consumer √](https://hub.docker.com/r/anjia0532/google-containers.resource_consumer/tags/)

[gcr.io/google-containers/rescheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-s390x/tags/)

[gcr.io/google-containers/rescheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-ppc64le/tags/)

[gcr.io/google-containers/rescheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm64/tags/)

[gcr.io/google-containers/rescheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm/tags/)

[gcr.io/google-containers/rescheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-amd64/tags/)

[gcr.io/google-containers/rescheduler √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler/tags/)

[gcr.io/google-containers/registry-promoter-test-image √](https://hub.docker.com/r/anjia0532/google-containers.registry-promoter-test-image/tags/)

[gcr.io/google-containers/redis-slave √](https://hub.docker.com/r/anjia0532/google-containers.redis-slave/tags/)

[gcr.io/google-containers/redis-install-3.2.0 √](https://hub.docker.com/r/anjia0532/google-containers.redis-install-3.2.0/tags/)

[gcr.io/google-containers/redis-install √](https://hub.docker.com/r/anjia0532/google-containers.redis-install/tags/)

[gcr.io/google-containers/redis √](https://hub.docker.com/r/anjia0532/google-containers.redis/tags/)

[gcr.io/google-containers/queue-health-poll √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-poll/tags/)

[gcr.io/google-containers/queue-health-graph √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-graph/tags/)

[gcr.io/google-containers/queue-health-base √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-base/tags/)

[gcr.io/google-containers/python √](https://hub.docker.com/r/anjia0532/google-containers.python/tags/)

[gcr.io/google-containers/publisher √](https://hub.docker.com/r/anjia0532/google-containers.publisher/tags/)

[gcr.io/google-containers/proxy-to-service √](https://hub.docker.com/r/anjia0532/google-containers.proxy-to-service/tags/)

[gcr.io/google-containers/prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-to-sd/tags/)

[gcr.io/google-containers/prometheus-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-dummy-exporter/tags/)

[gcr.io/google-containers/portforwardtester √](https://hub.docker.com/r/anjia0532/google-containers.portforwardtester/tags/)

[gcr.io/google-containers/porter √](https://hub.docker.com/r/anjia0532/google-containers.porter/tags/)

[gcr.io/google-containers/podmaster √](https://hub.docker.com/r/anjia0532/google-containers.podmaster/tags/)

[gcr.io/google-containers/perfdash √](https://hub.docker.com/r/anjia0532/google-containers.perfdash/tags/)

[gcr.io/google-containers/peer-finder √](https://hub.docker.com/r/anjia0532/google-containers.peer-finder/tags/)

[gcr.io/google-containers/pause-s390x √](https://hub.docker.com/r/anjia0532/google-containers.pause-s390x/tags/)

[gcr.io/google-containers/pause-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.pause-ppc64le/tags/)

[gcr.io/google-containers/pause-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm64/tags/)

[gcr.io/google-containers/pause-arm √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm/tags/)

[gcr.io/google-containers/pause-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-amd64/tags/)

[gcr.io/google-containers/pause √](https://hub.docker.com/r/anjia0532/google-containers.pause/tags/)

[gcr.io/google-containers/n-way-http √](https://hub.docker.com/r/anjia0532/google-containers.n-way-http/tags/)

[gcr.io/google-containers/kube-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy/tags/)

[gcr.io/google-containers/kube-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy/tags/)

[gcr.io/google-containers/nvidia-gpu-device-plugin √](https://hub.docker.com/r/anjia0532/google-containers.nvidia-gpu-device-plugin/tags/)

[gcr.io/google-containers/no-snat-test-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-proxy-amd64/tags/)

[gcr.io/google-containers/no-snat-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-amd64/tags/)

[gcr.io/google-containers/non-masquerade-daemon-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.non-masquerade-daemon-amd64/tags/)

[gcr.io/google-containers/nonewprivs √](https://hub.docker.com/r/anjia0532/google-containers.nonewprivs/tags/)

[gcr.io/google-containers/node-test-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm64/tags/)

[gcr.io/google-containers/node-test-arm √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm/tags/)

[gcr.io/google-containers/node-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-amd64/tags/)

[gcr.io/google-containers/node-test √](https://hub.docker.com/r/anjia0532/google-containers.node-test/tags/)

[gcr.io/google-containers/node-problem-detector √](https://hub.docker.com/r/anjia0532/google-containers.node-problem-detector/tags/)

[gcr.io/google-containers/node-perf-dash √](https://hub.docker.com/r/anjia0532/google-containers.node-perf-dash/tags/)

[gcr.io/google-containers/nodejs-election-client √](https://hub.docker.com/r/anjia0532/google-containers.nodejs-election-client/tags/)

[gcr.io/google-containers/node-conformance √](https://hub.docker.com/r/anjia0532/google-containers.node-conformance/tags/)

[gcr.io/google-containers/nginx-third-party √](https://hub.docker.com/r/anjia0532/google-containers.nginx-third-party/tags/)

[gcr.io/google-containers/nginx-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-ppc64le/tags/)

[gcr.io/google-containers/nginx-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm64/tags/)

[gcr.io/google-containers/nginx-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm/tags/)

[gcr.io/google-containers/nginx-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-amd64/tags/)

[gcr.io/google-containers/nginx-slim √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim/tags/)

[gcr.io/google-containers/nginx-scale √](https://hub.docker.com/r/anjia0532/google-containers.nginx-scale/tags/)

[gcr.io/google-containers/nginx-ingress-controller-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-ppc64le/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm64/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm/tags/)

[gcr.io/google-containers/nginx-ingress-controller-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-amd64/tags/)

[gcr.io/google-containers/kube-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-amd64/tags/)

[gcr.io/google-containers/kube-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-amd64/tags/)

[gcr.io/google-containers/nginx-ingress-controller √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller/tags/)

[gcr.io/google-containers/nginx-ingress √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress/tags/)

[gcr.io/google-containers/nginx √](https://hub.docker.com/r/anjia0532/google-containers.nginx/tags/)

[gcr.io/google-containers/nettest √](https://hub.docker.com/r/anjia0532/google-containers.nettest/tags/)

[gcr.io/google-containers/netproxy √](https://hub.docker.com/r/anjia0532/google-containers.netproxy/tags/)

[gcr.io/google-containers/netexec √](https://hub.docker.com/r/anjia0532/google-containers.netexec/tags/)

[gcr.io/google-containers/netd-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.netd-amd64/tags/)

[gcr.io/google-containers/netd √](https://hub.docker.com/r/anjia0532/google-containers.netd/tags/)

[gcr.io/google-containers/mysql-healthz √](https://hub.docker.com/r/anjia0532/google-containers.mysql-healthz/tags/)

[gcr.io/google-containers/mysql-galera √](https://hub.docker.com/r/anjia0532/google-containers.mysql-galera/tags/)

[gcr.io/google-containers/mungegithub √](https://hub.docker.com/r/anjia0532/google-containers.mungegithub/tags/)

[gcr.io/google-containers/mounttest-user √](https://hub.docker.com/r/anjia0532/google-containers.mounttest-user/tags/)

[gcr.io/google-containers/mounttest √](https://hub.docker.com/r/anjia0532/google-containers.mounttest/tags/)

[gcr.io/google-containers/mongodb-install √](https://hub.docker.com/r/anjia0532/google-containers.mongodb-install/tags/)

[gcr.io/google-containers/metrics-server-s390x √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-s390x/tags/)

[gcr.io/google-containers/metrics-server-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-ppc64le/tags/)

[gcr.io/google-containers/metrics-server-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm64/tags/)

[gcr.io/google-containers/metrics-server-arm √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm/tags/)

[gcr.io/google-containers/metrics-server-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-amd64/tags/)

[gcr.io/google-containers/metrics-server √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server/tags/)

[gcr.io/google-containers/metadata-proxy √](https://hub.docker.com/r/anjia0532/google-containers.metadata-proxy/tags/)

[gcr.io/google-containers/logs-generator √](https://hub.docker.com/r/anjia0532/google-containers.logs-generator/tags/)

[gcr.io/google-containers/logexporter √](https://hub.docker.com/r/anjia0532/google-containers.logexporter/tags/)

[gcr.io/google-containers/logexp √](https://hub.docker.com/r/anjia0532/google-containers.logexp/tags/)

[gcr.io/google-containers/loader √](https://hub.docker.com/r/anjia0532/google-containers.loader/tags/)

[gcr.io/google-containers/liveness √](https://hub.docker.com/r/anjia0532/google-containers.liveness/tags/)

[gcr.io/google-containers/leader-elector √](https://hub.docker.com/r/anjia0532/google-containers.leader-elector/tags/)

[gcr.io/google-containers/kube-ui √](https://hub.docker.com/r/anjia0532/google-containers.kube-ui/tags/)

[gcr.io/google-containers/kube-state-metrics-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-s390x/tags/)

[gcr.io/google-containers/kube-state-metrics-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-ppc64le/tags/)

[gcr.io/google-containers/kube-state-metrics-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm64/tags/)

[gcr.io/google-containers/kube-state-metrics-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm/tags/)

[gcr.io/google-containers/kube-state-metrics-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-amd64/tags/)

[gcr.io/google-containers/kube-state-metrics √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics/tags/)

[gcr.io/google-containers/kube-proxy-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm/tags/)

[gcr.io/google-containers/kube-proxy-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm/tags/)

[gcr.io/google-containers/kube-scheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-s390x/tags/)

[gcr.io/google-containers/kube-scheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-ppc64le/tags/)

[gcr.io/google-containers/kube-proxy-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm64/tags/)

[gcr.io/google-containers/kube-proxy-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm64/tags/)

[gcr.io/google-containers/kube-proxy-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-ppc64le/tags/)

[gcr.io/google-containers/kube-proxy-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-ppc64le/tags/)

[gcr.io/google-containers/kube-scheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm64/tags/)

[gcr.io/google-containers/kube-proxy-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-s390x/tags/)

[gcr.io/google-containers/kube-proxy-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-s390x/tags/)

[gcr.io/google-containers/kube-registry-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-registry-proxy/tags/)

[gcr.io/google-containers/kube-registry-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-registry-proxy/tags/)

[gcr.io/google-containers/kubernetes-dashboard √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard/tags/)

[gcr.io/google-containers/kubernetes-dashboard √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard/tags/)

[gcr.io/google-containers/kubernetes-dashboard-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-arm/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-arm/tags/)

[gcr.io/google-containers/kubernetes-dashboard-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-ppc64le/tags/)

[gcr.io/google-containers/kubernetes-dashboard-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-ppc64le/tags/)

[gcr.io/google-containers/kubernetes-dashboard-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-s390x/tags/)

[gcr.io/google-containers/kubernetes-dashboard-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-s390x/tags/)

[gcr.io/google-containers/kubernetes-kafka √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-kafka/tags/)

[gcr.io/google-containers/kubernetes-kafka √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-kafka/tags/)

[gcr.io/google-containers/kubernetes-zookeeper √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-zookeeper/tags/)

[gcr.io/google-containers/kubernetes-zookeeper √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-zookeeper/tags/)

[gcr.io/google-containers/kube-scheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm/tags/)

[gcr.io/google-containers/kube-scheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-amd64/tags/)

[gcr.io/google-containers/kube-scheduler √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler/tags/)

[gcr.io/google-containers/kube-scheduler √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler/tags/)

[gcr.io/google-containers/kube-scheduler √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler/tags/)

[gcr.io/google-containers/kubernetes-zookeeper √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-zookeeper/tags/)

[gcr.io/google-containers/kubernetes-kafka √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-kafka/tags/)

[gcr.io/google-containers/kubernetes-dashboard-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-s390x/tags/)

[gcr.io/google-containers/kube-scheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-ppc64le/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-arm/tags/)

[gcr.io/google-containers/kube-scheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-init-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-init-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm64/tags/)

[gcr.io/google-containers/kubernetes-dashboard-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-arm/tags/)

[gcr.io/google-containers/kubernetes-dashboard-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard-amd64/tags/)

[gcr.io/google-containers/kubernetes-dashboard √](https://hub.docker.com/r/anjia0532/google-containers.kubernetes-dashboard/tags/)

[gcr.io/google-containers/kube-registry-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-registry-proxy/tags/)

[gcr.io/google-containers/kube-scheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm/tags/)

[gcr.io/google-containers/kube-scheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm/tags/)

[gcr.io/google-containers/kube-proxy-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-s390x/tags/)

[gcr.io/google-containers/kube-scheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm64/tags/)

[gcr.io/google-containers/kube-scheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-arm64/tags/)

[gcr.io/google-containers/kube-proxy-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-ppc64le/tags/)

[gcr.io/google-containers/kube-scheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-ppc64le/tags/)

[gcr.io/google-containers/kube-scheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-ppc64le/tags/)

[gcr.io/google-containers/kube-scheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-s390x/tags/)

[gcr.io/google-containers/kube-scheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-scheduler-s390x/tags/)

[gcr.io/google-containers/kube-proxy-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm64/tags/)

[gcr.io/google-containers/kube-state-metrics √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics/tags/)

[gcr.io/google-containers/kube-state-metrics √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics/tags/)

[gcr.io/google-containers/kube-state-metrics-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-amd64/tags/)

[gcr.io/google-containers/kube-state-metrics-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-amd64/tags/)

[gcr.io/google-containers/kube-state-metrics-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm/tags/)

[gcr.io/google-containers/kube-state-metrics-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm/tags/)

[gcr.io/google-containers/kube-state-metrics-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm64/tags/)

[gcr.io/google-containers/kube-state-metrics-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-arm64/tags/)

[gcr.io/google-containers/kube-state-metrics-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-ppc64le/tags/)

[gcr.io/google-containers/kube-state-metrics-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-ppc64le/tags/)

[gcr.io/google-containers/kube-state-metrics-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-s390x/tags/)

[gcr.io/google-containers/kube-state-metrics-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-state-metrics-s390x/tags/)

[gcr.io/google-containers/kube-ui √](https://hub.docker.com/r/anjia0532/google-containers.kube-ui/tags/)

[gcr.io/google-containers/kube-ui √](https://hub.docker.com/r/anjia0532/google-containers.kube-ui/tags/)

[gcr.io/google-containers/leader-elector √](https://hub.docker.com/r/anjia0532/google-containers.leader-elector/tags/)

[gcr.io/google-containers/leader-elector √](https://hub.docker.com/r/anjia0532/google-containers.leader-elector/tags/)

[gcr.io/google-containers/liveness √](https://hub.docker.com/r/anjia0532/google-containers.liveness/tags/)

[gcr.io/google-containers/liveness √](https://hub.docker.com/r/anjia0532/google-containers.liveness/tags/)

[gcr.io/google-containers/loader √](https://hub.docker.com/r/anjia0532/google-containers.loader/tags/)

[gcr.io/google-containers/loader √](https://hub.docker.com/r/anjia0532/google-containers.loader/tags/)

[gcr.io/google-containers/logexp √](https://hub.docker.com/r/anjia0532/google-containers.logexp/tags/)

[gcr.io/google-containers/logexp √](https://hub.docker.com/r/anjia0532/google-containers.logexp/tags/)

[gcr.io/google-containers/kube-proxy-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-arm/tags/)

[gcr.io/google-containers/logexporter √](https://hub.docker.com/r/anjia0532/google-containers.logexporter/tags/)

[gcr.io/google-containers/logexporter √](https://hub.docker.com/r/anjia0532/google-containers.logexporter/tags/)

[gcr.io/google-containers/logs-generator √](https://hub.docker.com/r/anjia0532/google-containers.logs-generator/tags/)

[gcr.io/google-containers/logs-generator √](https://hub.docker.com/r/anjia0532/google-containers.logs-generator/tags/)

[gcr.io/google-containers/metadata-proxy √](https://hub.docker.com/r/anjia0532/google-containers.metadata-proxy/tags/)

[gcr.io/google-containers/metadata-proxy √](https://hub.docker.com/r/anjia0532/google-containers.metadata-proxy/tags/)

[gcr.io/google-containers/metrics-server √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server/tags/)

[gcr.io/google-containers/metrics-server √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server/tags/)

[gcr.io/google-containers/metrics-server-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-amd64/tags/)

[gcr.io/google-containers/metrics-server-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-amd64/tags/)

[gcr.io/google-containers/metrics-server-arm √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm/tags/)

[gcr.io/google-containers/metrics-server-arm √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm/tags/)

[gcr.io/google-containers/metrics-server-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm64/tags/)

[gcr.io/google-containers/metrics-server-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-arm64/tags/)

[gcr.io/google-containers/metrics-server-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-ppc64le/tags/)

[gcr.io/google-containers/metrics-server-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-ppc64le/tags/)

[gcr.io/google-containers/metrics-server-s390x √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-s390x/tags/)

[gcr.io/google-containers/metrics-server-s390x √](https://hub.docker.com/r/anjia0532/google-containers.metrics-server-s390x/tags/)

[gcr.io/google-containers/kube-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy-amd64/tags/)

[gcr.io/google-containers/mongodb-install √](https://hub.docker.com/r/anjia0532/google-containers.mongodb-install/tags/)

[gcr.io/google-containers/mongodb-install √](https://hub.docker.com/r/anjia0532/google-containers.mongodb-install/tags/)

[gcr.io/google-containers/mounttest √](https://hub.docker.com/r/anjia0532/google-containers.mounttest/tags/)

[gcr.io/google-containers/mounttest √](https://hub.docker.com/r/anjia0532/google-containers.mounttest/tags/)

[gcr.io/google-containers/mounttest-user √](https://hub.docker.com/r/anjia0532/google-containers.mounttest-user/tags/)

[gcr.io/google-containers/mounttest-user √](https://hub.docker.com/r/anjia0532/google-containers.mounttest-user/tags/)

[gcr.io/google-containers/mungegithub √](https://hub.docker.com/r/anjia0532/google-containers.mungegithub/tags/)

[gcr.io/google-containers/mungegithub √](https://hub.docker.com/r/anjia0532/google-containers.mungegithub/tags/)

[gcr.io/google-containers/mysql-galera √](https://hub.docker.com/r/anjia0532/google-containers.mysql-galera/tags/)

[gcr.io/google-containers/mysql-galera √](https://hub.docker.com/r/anjia0532/google-containers.mysql-galera/tags/)

[gcr.io/google-containers/mysql-healthz √](https://hub.docker.com/r/anjia0532/google-containers.mysql-healthz/tags/)

[gcr.io/google-containers/mysql-healthz √](https://hub.docker.com/r/anjia0532/google-containers.mysql-healthz/tags/)

[gcr.io/google-containers/netd √](https://hub.docker.com/r/anjia0532/google-containers.netd/tags/)

[gcr.io/google-containers/kube-proxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-proxy/tags/)

[gcr.io/google-containers/netd-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.netd-amd64/tags/)

[gcr.io/google-containers/netd √](https://hub.docker.com/r/anjia0532/google-containers.netd/tags/)

[gcr.io/google-containers/kube-nethealth-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-nethealth-amd64/tags/)

[gcr.io/google-containers/netd-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.netd-amd64/tags/)

[gcr.io/google-containers/netexec √](https://hub.docker.com/r/anjia0532/google-containers.netexec/tags/)

[gcr.io/google-containers/kubelet-to-gcm √](https://hub.docker.com/r/anjia0532/google-containers.kubelet-to-gcm/tags/)

[gcr.io/google-containers/netproxy √](https://hub.docker.com/r/anjia0532/google-containers.netproxy/tags/)

[gcr.io/google-containers/netexec √](https://hub.docker.com/r/anjia0532/google-containers.netexec/tags/)

[gcr.io/google-containers/netproxy √](https://hub.docker.com/r/anjia0532/google-containers.netproxy/tags/)

[gcr.io/google-containers/nettest √](https://hub.docker.com/r/anjia0532/google-containers.nettest/tags/)

[gcr.io/google-containers/kubekins-test √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-test/tags/)

[gcr.io/google-containers/nettest √](https://hub.docker.com/r/anjia0532/google-containers.nettest/tags/)

[gcr.io/google-containers/nginx √](https://hub.docker.com/r/anjia0532/google-containers.nginx/tags/)

[gcr.io/google-containers/kubekins-job-builder √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-job-builder/tags/)

[gcr.io/google-containers/nginx-ingress √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress/tags/)

[gcr.io/google-containers/nginx √](https://hub.docker.com/r/anjia0532/google-containers.nginx/tags/)

[gcr.io/google-containers/nginx-ingress √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress/tags/)

[gcr.io/google-containers/kubekins-e2e √](https://hub.docker.com/r/anjia0532/google-containers.kubekins-e2e/tags/)

[gcr.io/google-containers/nginx-ingress-controller √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller/tags/)

[gcr.io/google-containers/kube-keepalived-vip √](https://hub.docker.com/r/anjia0532/google-containers.kube-keepalived-vip/tags/)

[gcr.io/google-containers/nginx-ingress-controller-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-amd64/tags/)

[gcr.io/google-containers/nginx-ingress-controller √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller/tags/)

[gcr.io/google-containers/kube-haproxy √](https://hub.docker.com/r/anjia0532/google-containers.kube-haproxy/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm/tags/)

[gcr.io/google-containers/nginx-ingress-controller-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-amd64/tags/)

[gcr.io/google-containers/kubedns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-ppc64le/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm64/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm/tags/)

[gcr.io/google-containers/kube-dns-perf-client-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dns-perf-client-amd64/tags/)

[gcr.io/google-containers/nginx-ingress-controller-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-arm64/tags/)

[gcr.io/google-containers/nginx-ingress-controller-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-ppc64le/tags/)

[gcr.io/google-containers/kube-dnsmasq-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-ppc64le/tags/)

[gcr.io/google-containers/nginx-scale √](https://hub.docker.com/r/anjia0532/google-containers.nginx-scale/tags/)

[gcr.io/google-containers/nginx-ingress-controller-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-ingress-controller-ppc64le/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm64/tags/)

[gcr.io/google-containers/nginx-scale √](https://hub.docker.com/r/anjia0532/google-containers.nginx-scale/tags/)

[gcr.io/google-containers/nginx-slim √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim/tags/)

[gcr.io/google-containers/kube-dnsmasq-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-arm/tags/)

[gcr.io/google-containers/nginx-slim √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim/tags/)

[gcr.io/google-containers/nginx-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-amd64/tags/)

[gcr.io/google-containers/kube-dnsmasq-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-dnsmasq-amd64/tags/)

[gcr.io/google-containers/nginx-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-amd64/tags/)

[gcr.io/google-containers/nginx-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm/tags/)

[gcr.io/google-containers/kubedns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm64/tags/)

[gcr.io/google-containers/nginx-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm64/tags/)

[gcr.io/google-containers/nginx-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm/tags/)

[gcr.io/google-containers/kubedns-arm √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-arm/tags/)

[gcr.io/google-containers/nginx-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-ppc64le/tags/)

[gcr.io/google-containers/nginx-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-arm64/tags/)

[gcr.io/google-containers/kubedns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kubedns-amd64/tags/)

[gcr.io/google-containers/nginx-third-party √](https://hub.docker.com/r/anjia0532/google-containers.nginx-third-party/tags/)

[gcr.io/google-containers/nginx-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.nginx-slim-ppc64le/tags/)

[gcr.io/google-containers/kube-discovery-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm64/tags/)

[gcr.io/google-containers/node-conformance √](https://hub.docker.com/r/anjia0532/google-containers.node-conformance/tags/)

[gcr.io/google-containers/kube-discovery-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-arm/tags/)

[gcr.io/google-containers/nginx-third-party √](https://hub.docker.com/r/anjia0532/google-containers.nginx-third-party/tags/)

[gcr.io/google-containers/nodejs-election-client √](https://hub.docker.com/r/anjia0532/google-containers.nodejs-election-client/tags/)

[gcr.io/google-containers/kube-discovery-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-discovery-amd64/tags/)

[gcr.io/google-containers/node-conformance √](https://hub.docker.com/r/anjia0532/google-containers.node-conformance/tags/)

[gcr.io/google-containers/node-perf-dash √](https://hub.docker.com/r/anjia0532/google-containers.node-perf-dash/tags/)

[gcr.io/google-containers/kubedash √](https://hub.docker.com/r/anjia0532/google-containers.kubedash/tags/)

[gcr.io/google-containers/nodejs-election-client √](https://hub.docker.com/r/anjia0532/google-containers.nodejs-election-client/tags/)

[gcr.io/google-containers/node-problem-detector √](https://hub.docker.com/r/anjia0532/google-containers.node-problem-detector/tags/)

[gcr.io/google-containers/kubectl √](https://hub.docker.com/r/anjia0532/google-containers.kubectl/tags/)

[gcr.io/google-containers/node-perf-dash √](https://hub.docker.com/r/anjia0532/google-containers.node-perf-dash/tags/)

[gcr.io/google-containers/node-test √](https://hub.docker.com/r/anjia0532/google-containers.node-test/tags/)

[gcr.io/google-containers/node-problem-detector √](https://hub.docker.com/r/anjia0532/google-containers.node-problem-detector/tags/)

[gcr.io/google-containers/kube-cross √](https://hub.docker.com/r/anjia0532/google-containers.kube-cross/tags/)

[gcr.io/google-containers/node-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-amd64/tags/)

[gcr.io/google-containers/node-test √](https://hub.docker.com/r/anjia0532/google-containers.node-test/tags/)

[gcr.io/google-containers/node-test-arm √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm/tags/)

[gcr.io/google-containers/node-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-amd64/tags/)

[gcr.io/google-containers/node-test-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm64/tags/)

[gcr.io/google-containers/node-test-arm √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm/tags/)

[gcr.io/google-containers/nonewprivs √](https://hub.docker.com/r/anjia0532/google-containers.nonewprivs/tags/)

[gcr.io/google-containers/node-test-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.node-test-arm64/tags/)

[gcr.io/google-containers/non-masquerade-daemon-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.non-masquerade-daemon-amd64/tags/)

[gcr.io/google-containers/nonewprivs √](https://hub.docker.com/r/anjia0532/google-containers.nonewprivs/tags/)

[gcr.io/google-containers/no-snat-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-amd64/tags/)

[gcr.io/google-containers/non-masquerade-daemon-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.non-masquerade-daemon-amd64/tags/)

[gcr.io/google-containers/no-snat-test-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-proxy-amd64/tags/)

[gcr.io/google-containers/no-snat-test-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-amd64/tags/)

[gcr.io/google-containers/nvidia-gpu-device-plugin √](https://hub.docker.com/r/anjia0532/google-containers.nvidia-gpu-device-plugin/tags/)

[gcr.io/google-containers/no-snat-test-proxy-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.no-snat-test-proxy-amd64/tags/)

[gcr.io/google-containers/kube-controller-manager-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager-s390x/tags/)

[gcr.io/google-containers/n-way-http √](https://hub.docker.com/r/anjia0532/google-containers.n-way-http/tags/)

[gcr.io/google-containers/nvidia-gpu-device-plugin √](https://hub.docker.com/r/anjia0532/google-containers.nvidia-gpu-device-plugin/tags/)

[gcr.io/google-containers/pause √](https://hub.docker.com/r/anjia0532/google-containers.pause/tags/)

[gcr.io/google-containers/n-way-http √](https://hub.docker.com/r/anjia0532/google-containers.n-way-http/tags/)

[gcr.io/google-containers/pause-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-amd64/tags/)

[gcr.io/google-containers/pause √](https://hub.docker.com/r/anjia0532/google-containers.pause/tags/)

[gcr.io/google-containers/pause-arm √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm/tags/)

[gcr.io/google-containers/pause-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-amd64/tags/)

[gcr.io/google-containers/pause-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm64/tags/)

[gcr.io/google-containers/pause-arm √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm/tags/)

[gcr.io/google-containers/pause-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.pause-ppc64le/tags/)

[gcr.io/google-containers/pause-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.pause-arm64/tags/)

[gcr.io/google-containers/pause-s390x √](https://hub.docker.com/r/anjia0532/google-containers.pause-s390x/tags/)

[gcr.io/google-containers/pause-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.pause-ppc64le/tags/)

[gcr.io/google-containers/peer-finder √](https://hub.docker.com/r/anjia0532/google-containers.peer-finder/tags/)

[gcr.io/google-containers/pause-s390x √](https://hub.docker.com/r/anjia0532/google-containers.pause-s390x/tags/)

[gcr.io/google-containers/kube-controller-manager-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager-ppc64le/tags/)

[gcr.io/google-containers/perfdash √](https://hub.docker.com/r/anjia0532/google-containers.perfdash/tags/)

[gcr.io/google-containers/peer-finder √](https://hub.docker.com/r/anjia0532/google-containers.peer-finder/tags/)

[gcr.io/google-containers/podmaster √](https://hub.docker.com/r/anjia0532/google-containers.podmaster/tags/)

[gcr.io/google-containers/perfdash √](https://hub.docker.com/r/anjia0532/google-containers.perfdash/tags/)

[gcr.io/google-containers/porter √](https://hub.docker.com/r/anjia0532/google-containers.porter/tags/)

[gcr.io/google-containers/podmaster √](https://hub.docker.com/r/anjia0532/google-containers.podmaster/tags/)

[gcr.io/google-containers/portforwardtester √](https://hub.docker.com/r/anjia0532/google-containers.portforwardtester/tags/)

[gcr.io/google-containers/porter √](https://hub.docker.com/r/anjia0532/google-containers.porter/tags/)

[gcr.io/google-containers/prometheus-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-dummy-exporter/tags/)

[gcr.io/google-containers/portforwardtester √](https://hub.docker.com/r/anjia0532/google-containers.portforwardtester/tags/)

[gcr.io/google-containers/prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-to-sd/tags/)

[gcr.io/google-containers/prometheus-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-dummy-exporter/tags/)

[gcr.io/google-containers/proxy-to-service √](https://hub.docker.com/r/anjia0532/google-containers.proxy-to-service/tags/)

[gcr.io/google-containers/prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.prometheus-to-sd/tags/)

[gcr.io/google-containers/proxy-to-service √](https://hub.docker.com/r/anjia0532/google-containers.proxy-to-service/tags/)

[gcr.io/google-containers/publisher √](https://hub.docker.com/r/anjia0532/google-containers.publisher/tags/)

[gcr.io/google-containers/python √](https://hub.docker.com/r/anjia0532/google-containers.python/tags/)

[gcr.io/google-containers/publisher √](https://hub.docker.com/r/anjia0532/google-containers.publisher/tags/)

[gcr.io/google-containers/kube-controller-manager-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager-arm64/tags/)

[gcr.io/google-containers/python √](https://hub.docker.com/r/anjia0532/google-containers.python/tags/)

[gcr.io/google-containers/queue-health-base √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-base/tags/)

[gcr.io/google-containers/queue-health-base √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-base/tags/)

[gcr.io/google-containers/queue-health-graph √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-graph/tags/)

[gcr.io/google-containers/queue-health-graph √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-graph/tags/)

[gcr.io/google-containers/queue-health-poll √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-poll/tags/)

[gcr.io/google-containers/queue-health-poll √](https://hub.docker.com/r/anjia0532/google-containers.queue-health-poll/tags/)

[gcr.io/google-containers/redis √](https://hub.docker.com/r/anjia0532/google-containers.redis/tags/)

[gcr.io/google-containers/redis √](https://hub.docker.com/r/anjia0532/google-containers.redis/tags/)

[gcr.io/google-containers/redis-install √](https://hub.docker.com/r/anjia0532/google-containers.redis-install/tags/)

[gcr.io/google-containers/redis-install √](https://hub.docker.com/r/anjia0532/google-containers.redis-install/tags/)

[gcr.io/google-containers/redis-install-3.2.0 √](https://hub.docker.com/r/anjia0532/google-containers.redis-install-3.2.0/tags/)

[gcr.io/google-containers/redis-install-3.2.0 √](https://hub.docker.com/r/anjia0532/google-containers.redis-install-3.2.0/tags/)

[gcr.io/google-containers/redis-slave √](https://hub.docker.com/r/anjia0532/google-containers.redis-slave/tags/)

[gcr.io/google-containers/redis-slave √](https://hub.docker.com/r/anjia0532/google-containers.redis-slave/tags/)

[gcr.io/google-containers/registry-promoter-test-image √](https://hub.docker.com/r/anjia0532/google-containers.registry-promoter-test-image/tags/)

[gcr.io/google-containers/registry-promoter-test-image √](https://hub.docker.com/r/anjia0532/google-containers.registry-promoter-test-image/tags/)

[gcr.io/google-containers/kube-controller-manager-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager-arm/tags/)

[gcr.io/google-containers/rescheduler √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler/tags/)

[gcr.io/google-containers/rescheduler √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler/tags/)

[gcr.io/google-containers/rescheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-amd64/tags/)

[gcr.io/google-containers/rescheduler-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-amd64/tags/)

[gcr.io/google-containers/rescheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm/tags/)

[gcr.io/google-containers/rescheduler-arm √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm/tags/)

[gcr.io/google-containers/rescheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm64/tags/)

[gcr.io/google-containers/rescheduler-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-arm64/tags/)

[gcr.io/google-containers/rescheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-ppc64le/tags/)

[gcr.io/google-containers/rescheduler-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-ppc64le/tags/)

[gcr.io/google-containers/rescheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-s390x/tags/)

[gcr.io/google-containers/rescheduler-s390x √](https://hub.docker.com/r/anjia0532/google-containers.rescheduler-s390x/tags/)

[gcr.io/google-containers/resource_consumer √](https://hub.docker.com/r/anjia0532/google-containers.resource_consumer/tags/)

[gcr.io/google-containers/rethinkdb √](https://hub.docker.com/r/anjia0532/google-containers.rethinkdb/tags/)

[gcr.io/google-containers/resource_consumer √](https://hub.docker.com/r/anjia0532/google-containers.resource_consumer/tags/)

[gcr.io/google-containers/rethinkdb √](https://hub.docker.com/r/anjia0532/google-containers.rethinkdb/tags/)

[gcr.io/google-containers/sd-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.sd-dummy-exporter/tags/)

[gcr.io/google-containers/serve_hostname √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname/tags/)

[gcr.io/google-containers/sd-dummy-exporter √](https://hub.docker.com/r/anjia0532/google-containers.sd-dummy-exporter/tags/)

[gcr.io/google-containers/kube-controller-manager-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager-amd64/tags/)

[gcr.io/google-containers/serve_hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-amd64/tags/)

[gcr.io/google-containers/serve_hostname √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname/tags/)

[gcr.io/google-containers/serve-hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-amd64/tags/)

[gcr.io/google-containers/serve_hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-amd64/tags/)

[gcr.io/google-containers/serve_hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm/tags/)

[gcr.io/google-containers/serve-hostname-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-amd64/tags/)

[gcr.io/google-containers/serve-hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm/tags/)

[gcr.io/google-containers/serve_hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm/tags/)

[gcr.io/google-containers/serve_hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm64/tags/)

[gcr.io/google-containers/serve-hostname-arm √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm/tags/)

[gcr.io/google-containers/serve-hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm64/tags/)

[gcr.io/google-containers/serve_hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-arm64/tags/)

[gcr.io/google-containers/serve_hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-ppc64le/tags/)

[gcr.io/google-containers/kube-controller-manager √](https://hub.docker.com/r/anjia0532/google-containers.kube-controller-manager/tags/)

[gcr.io/google-containers/serve-hostname-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-arm64/tags/)

[gcr.io/google-containers/serve-hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-ppc64le/tags/)

[gcr.io/google-containers/serve_hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-ppc64le/tags/)

[gcr.io/google-containers/serve_hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-s390x/tags/)

[gcr.io/google-containers/serve-hostname-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-ppc64le/tags/)

[gcr.io/google-containers/serve-hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-s390x/tags/)

[gcr.io/google-containers/serve_hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve_hostname-s390x/tags/)

[gcr.io/google-containers/servicelb √](https://hub.docker.com/r/anjia0532/google-containers.servicelb/tags/)

[gcr.io/google-containers/serve-hostname-s390x √](https://hub.docker.com/r/anjia0532/google-containers.serve-hostname-s390x/tags/)

[gcr.io/google-containers/shame-mailer √](https://hub.docker.com/r/anjia0532/google-containers.shame-mailer/tags/)

[gcr.io/google-containers/servicelb √](https://hub.docker.com/r/anjia0532/google-containers.servicelb/tags/)

[gcr.io/google-containers/shyamjvs-logexp √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-logexp/tags/)

[gcr.io/google-containers/shame-mailer √](https://hub.docker.com/r/anjia0532/google-containers.shame-mailer/tags/)

[gcr.io/google-containers/shyamjvs-prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-prometheus-to-sd/tags/)

[gcr.io/google-containers/shyamjvs-logexp √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-logexp/tags/)

[gcr.io/google-containers/skydns √](https://hub.docker.com/r/anjia0532/google-containers.skydns/tags/)

[gcr.io/google-containers/shyamjvs-prometheus-to-sd √](https://hub.docker.com/r/anjia0532/google-containers.shyamjvs-prometheus-to-sd/tags/)

[gcr.io/google-containers/kube-apiserver-s390x √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver-s390x/tags/)

[gcr.io/google-containers/skydns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-amd64/tags/)

[gcr.io/google-containers/skydns √](https://hub.docker.com/r/anjia0532/google-containers.skydns/tags/)

[gcr.io/google-containers/skydns-arm √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm/tags/)

[gcr.io/google-containers/skydns-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-amd64/tags/)

[gcr.io/google-containers/skydns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm64/tags/)

[gcr.io/google-containers/skydns-arm √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm/tags/)

[gcr.io/google-containers/skydns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.skydns-ppc64le/tags/)

[gcr.io/google-containers/skydns-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.skydns-arm64/tags/)

[gcr.io/google-containers/slo-monitor √](https://hub.docker.com/r/anjia0532/google-containers.slo-monitor/tags/)

[gcr.io/google-containers/skydns-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.skydns-ppc64le/tags/)

[gcr.io/google-containers/slo-monitor √](https://hub.docker.com/r/anjia0532/google-containers.slo-monitor/tags/)

[gcr.io/google-containers/spark √](https://hub.docker.com/r/anjia0532/google-containers.spark/tags/)

[gcr.io/google-containers/spark √](https://hub.docker.com/r/anjia0532/google-containers.spark/tags/)

[gcr.io/google-containers/spark-base √](https://hub.docker.com/r/anjia0532/google-containers.spark-base/tags/)

[gcr.io/google-containers/spark-base √](https://hub.docker.com/r/anjia0532/google-containers.spark-base/tags/)

[gcr.io/google-containers/spark-driver √](https://hub.docker.com/r/anjia0532/google-containers.spark-driver/tags/)

[gcr.io/google-containers/spark-driver √](https://hub.docker.com/r/anjia0532/google-containers.spark-driver/tags/)

[gcr.io/google-containers/spark-master √](https://hub.docker.com/r/anjia0532/google-containers.spark-master/tags/)

[gcr.io/google-containers/spark-master √](https://hub.docker.com/r/anjia0532/google-containers.spark-master/tags/)

[gcr.io/google-containers/kube-apiserver-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver-ppc64le/tags/)

[gcr.io/google-containers/spark-worker √](https://hub.docker.com/r/anjia0532/google-containers.spark-worker/tags/)

[gcr.io/google-containers/spark-worker √](https://hub.docker.com/r/anjia0532/google-containers.spark-worker/tags/)

[gcr.io/google-containers/spartakus-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.spartakus-amd64/tags/)

[gcr.io/google-containers/spartakus-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.spartakus-amd64/tags/)

[gcr.io/google-containers/startup-script √](https://hub.docker.com/r/anjia0532/google-containers.startup-script/tags/)

[gcr.io/google-containers/startup-script √](https://hub.docker.com/r/anjia0532/google-containers.startup-script/tags/)

[gcr.io/google-containers/stress √](https://hub.docker.com/r/anjia0532/google-containers.stress/tags/)

[gcr.io/google-containers/stress √](https://hub.docker.com/r/anjia0532/google-containers.stress/tags/)

[gcr.io/google-containers/submit-queue √](https://hub.docker.com/r/anjia0532/google-containers.submit-queue/tags/)

[gcr.io/google-containers/submit-queue √](https://hub.docker.com/r/anjia0532/google-containers.submit-queue/tags/)

[gcr.io/google-containers/tensorflow-gpu-notebook √](https://hub.docker.com/r/anjia0532/google-containers.tensorflow-gpu-notebook/tags/)

[gcr.io/google-containers/tensorflow-gpu-notebook √](https://hub.docker.com/r/anjia0532/google-containers.tensorflow-gpu-notebook/tags/)

[gcr.io/google-containers/test_subdir_1 √](https://hub.docker.com/r/anjia0532/google-containers.test_subdir_1/tags/)

[gcr.io/google-containers/test_subdir_1 √](https://hub.docker.com/r/anjia0532/google-containers.test_subdir_1/tags/)

[gcr.io/google-containers/test-webserver √](https://hub.docker.com/r/anjia0532/google-containers.test-webserver/tags/)

[gcr.io/google-containers/test-webserver √](https://hub.docker.com/r/anjia0532/google-containers.test-webserver/tags/)

[gcr.io/google-containers/tf-models √](https://hub.docker.com/r/anjia0532/google-containers.tf-models/tags/)

[gcr.io/google-containers/kube-apiserver-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver-arm64/tags/)

[gcr.io/google-containers/tiny-glibc-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-amd64/tags/)

[gcr.io/google-containers/tf-models √](https://hub.docker.com/r/anjia0532/google-containers.tf-models/tags/)

[gcr.io/google-containers/tiny-glibc-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-amd64/tags/)

[gcr.io/google-containers/tiny-glibc-arm √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm/tags/)

[gcr.io/google-containers/tiny-glibc-arm √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm/tags/)

[gcr.io/google-containers/tiny-glibc-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm64/tags/)

[gcr.io/google-containers/tiny-glibc-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-arm64/tags/)

[gcr.io/google-containers/tiny-glibc-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-ppc64le/tags/)

[gcr.io/google-containers/tiny-glibc-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.tiny-glibc-ppc64le/tags/)

[gcr.io/google-containers/toolbox √](https://hub.docker.com/r/anjia0532/google-containers.toolbox/tags/)

[gcr.io/google-containers/toolbox √](https://hub.docker.com/r/anjia0532/google-containers.toolbox/tags/)

[gcr.io/google-containers/ubuntu √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu/tags/)

[gcr.io/google-containers/ubuntu √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu/tags/)

[gcr.io/google-containers/ubuntu-nvidia-driver-installer √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-nvidia-driver-installer/tags/)

[gcr.io/google-containers/ubuntu-nvidia-driver-installer √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-nvidia-driver-installer/tags/)

[gcr.io/google-containers/ubuntu-slim √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim/tags/)

[gcr.io/google-containers/ubuntu-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-amd64/tags/)

[gcr.io/google-containers/ubuntu-slim √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim/tags/)

[gcr.io/google-containers/kube-apiserver-arm √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver-arm/tags/)

[gcr.io/google-containers/ubuntu-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm/tags/)

[gcr.io/google-containers/ubuntu-slim-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-amd64/tags/)

[gcr.io/google-containers/ubuntu-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm64/tags/)

[gcr.io/google-containers/ubuntu-slim-arm √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm/tags/)

[gcr.io/google-containers/ubuntu-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-ppc64le/tags/)

[gcr.io/google-containers/ubuntu-slim-arm64 √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-arm64/tags/)

[gcr.io/google-containers/update-demo √](https://hub.docker.com/r/anjia0532/google-containers.update-demo/tags/)

[gcr.io/google-containers/ubuntu-slim-ppc64le √](https://hub.docker.com/r/anjia0532/google-containers.ubuntu-slim-ppc64le/tags/)

[gcr.io/google-containers/update-demo √](https://hub.docker.com/r/anjia0532/google-containers.update-demo/tags/)

[gcr.io/google-containers/volume-ceph √](https://hub.docker.com/r/anjia0532/google-containers.volume-ceph/tags/)

[gcr.io/google-containers/volume-csi √](https://hub.docker.com/r/anjia0532/google-containers.volume-csi/tags/)

[gcr.io/google-containers/volume-ceph √](https://hub.docker.com/r/anjia0532/google-containers.volume-ceph/tags/)

[gcr.io/google-containers/volume-csi √](https://hub.docker.com/r/anjia0532/google-containers.volume-csi/tags/)

[gcr.io/google-containers/volume-gluster √](https://hub.docker.com/r/anjia0532/google-containers.volume-gluster/tags/)

[gcr.io/google-containers/volume-iscsi √](https://hub.docker.com/r/anjia0532/google-containers.volume-iscsi/tags/)

[gcr.io/google-containers/volume-gluster √](https://hub.docker.com/r/anjia0532/google-containers.volume-gluster/tags/)

[gcr.io/google-containers/volume-nfs √](https://hub.docker.com/r/anjia0532/google-containers.volume-nfs/tags/)

[gcr.io/google-containers/volume-iscsi √](https://hub.docker.com/r/anjia0532/google-containers.volume-iscsi/tags/)

[gcr.io/google-containers/volume-rbd √](https://hub.docker.com/r/anjia0532/google-containers.volume-rbd/tags/)

[gcr.io/google-containers/volume-nfs √](https://hub.docker.com/r/anjia0532/google-containers.volume-nfs/tags/)

[gcr.io/google-containers/vpa-admission-controller √](https://hub.docker.com/r/anjia0532/google-containers.vpa-admission-controller/tags/)

[gcr.io/google-containers/kube-apiserver-amd64 √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver-amd64/tags/)

[gcr.io/google-containers/vpa-recommender √](https://hub.docker.com/r/anjia0532/google-containers.vpa-recommender/tags/)

[gcr.io/google-containers/volume-rbd √](https://hub.docker.com/r/anjia0532/google-containers.volume-rbd/tags/)

[gcr.io/google-containers/vpa-updater √](https://hub.docker.com/r/anjia0532/google-containers.vpa-updater/tags/)

[gcr.io/google-containers/webhooks-publisher √](https://hub.docker.com/r/anjia0532/google-containers.webhooks-publisher/tags/)

[gcr.io/google-containers/vpa-admission-controller √](https://hub.docker.com/r/anjia0532/google-containers.vpa-admission-controller/tags/)

[gcr.io/google-containers/zeppelin √](https://hub.docker.com/r/anjia0532/google-containers.zeppelin/tags/)

[gcr.io/google-containers/vpa-recommender √](https://hub.docker.com/r/anjia0532/google-containers.vpa-recommender/tags/)

[gcr.io/google-containers/zeppelin-proxy √](https://hub.docker.com/r/anjia0532/google-containers.zeppelin-proxy/tags/)

[gcr.io/google-containers/vpa-updater √](https://hub.docker.com/r/anjia0532/google-containers.vpa-updater/tags/)

[gcr.io/google-containers/zookeeper-install √](https://hub.docker.com/r/anjia0532/google-containers.zookeeper-install/tags/)

[gcr.io/google-containers/webhooks-publisher √](https://hub.docker.com/r/anjia0532/google-containers.webhooks-publisher/tags/)

[gcr.io/google-containers/kube-apiserver √](https://hub.docker.com/r/anjia0532/google-containers.kube-apiserver/tags/)

[gcr.io/google-containers/zookeeper-install-3.5.0-alpha √](https://hub.docker.com/r/anjia0532/google-containers.zookeeper-install-3.5.0-alpha/tags/)

