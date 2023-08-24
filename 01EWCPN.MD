# 1. East West cross provider networking.
  
## As a web admin I want to add resiliency to my site, so I need to replicate my backend services without over exposing my service to the public internet.

### Tasks

- [x] Test Wireguard > FAILED > will not run, needs to insert kernel module.
- [x] Test Tailscale > SUCCESS > needs testing if it will run in akash (no marketplace sdls). REF:https://tailscale.com/kb/1108/cloudrun/
  - [x] magic dns works in pod once nameserver 100.100.100.100 is added to /etc/resolv.conf (known full/short host name can be used by services to replicate/cluster).
  - [ ] create bundle to demo, leverage confidential container to protect the key.
