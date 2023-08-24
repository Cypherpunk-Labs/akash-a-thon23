# 1. East West cross provider networking.
  
## As a web admin I want to add resiliency to my site, so I need to replicate my backend services without over exposing my service to the public internet.

### Tasks

- Wireguard will not run, needs to insert kernel module.
- [x] Tailscale needs testing if it will run in akash (no marketplace sdls). YES
- https://tailscale.com/kb/1108/cloudrun/
- [x] magic dns works in pod once nameserver 100.100.100.100 is added to /etc/resolv.conf (known full/short host name can be used by services to replicate/cluster).
