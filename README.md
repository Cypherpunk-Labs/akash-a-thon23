# akash-a-thon23
Akash-a-thon 2023 https://dorahacks.io/hackathon/akash-a-thon/hackers

Areas of interest to build upon;

1. East West cross provider networking.
  - As a web admin I want to add resiliency to my site, so I need to replicate my backend services without over exposing my service to the public internet.
    - Wireguard will not run, needs to insert kernel module.
    - Tailscale needs testing if it will run in akash (no marketplace sdls).
3. Confidential Containers
  - As a web admin I want to ensure I can protect any data I may collect in accordance with the law.
    - https://github.com/confidential-containers
    - https://www.redhat.com/en/blog/how-use-confidential-containers-without-confidential-hardware
    - https://rcarrata.com/openshift/sandbox-containers/
    - https://www.edgeless.systems/products/ego/  
4. Cluster Autoscaler
  - As a Provider I want to minimise my energy costs by scaling down excess capacity, and power back up as demand increases.
    - https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/cloudprovider/externalgrpc/README.md
    - https://isitobservable.io/observability/kubernetes/how-to-autoscale-in-kubernetes-and-how-to-observe-scaling-decisions
    - https://samos-it.com/posts/gke-custom-oss-cluster-autoscaler.html
    - https://github.com/openshift/cluster-autoscaler-operator
