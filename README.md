# akash-a-thon23
Akash-a-thon 2023 https://dorahacks.io/hackathon/akash-a-thon/hackers

Areas of interest to build upon;

1. East West cross provider networking.
  - As a web admin I want to add resiliency to my site, so I need to replicate my backend services without over exposing my service to the public internet.
    - Wireguard will not run, needs to insert kernel module.
    - [x] Tailscale needs testing if it will run in akash (no marketplace sdls). YES
      - https://tailscale.com/kb/1108/cloudrun/
      - [x] magic dns works in pod once nameserver 100.100.100.100 is added to /etc/resolv.conf (known full/short host name can be used by services to replicate/cluster).
3. Confidential Containers
  - As a web admin I want to ensure I can protect any data I may collect in accordance with the law.
    - https://github.com/confidential-containers
      - [x] operator install failing (intel SGX)
    - https://www.redhat.com/en/blog/how-use-confidential-containers-without-confidential-hardware
    - https://rcarrata.com/openshift/sandbox-containers/
    - https://github.com/inclavare-containers/inclavare-containers
    - [x] test for TPM, https://unix.stackexchange.com/questions/341629/how-to-determine-if-computer-has-tpm-trusted-platform-module-available
    - Kata-containers
      - https://www.programmersought.com/article/51324774363/
      - https://blog.niflheim.cc/posts/kata_containers_raspberry/
      - Gist: k3s handles containerd so need to patch config to make work.
    - [ ] POC
      - [x] install operator https://github.com/kata-containers/kata-containers/blob/3.1.3/tools/packaging/kata-deploy/README.md
      - [ ] mutate deployment
      - [ ] stretch goal extend SDL
    - All above need operators installed into k8s (Can only obfuscate inside process)
    - https://www.edgeless.systems/products/ego/
    - https://github.com/awnumar/memguard
    - https://sgx101.gitbook.io/sgx101/sgx-bootstrap/overview
4. Cluster Autoscaler
  - As a Provider I want to minimise my energy costs by scaling down excess capacity, and power back up as demand increases.
    - https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/cloudprovider/externalgrpc/README.md
    - https://isitobservable.io/observability/kubernetes/how-to-autoscale-in-kubernetes-and-how-to-observe-scaling-decisions
    - https://samos-it.com/posts/gke-custom-oss-cluster-autoscaler.html
    - https://github.com/openshift/cluster-autoscaler-operator
