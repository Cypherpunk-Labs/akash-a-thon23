# 1. East West cross provider networking.

## Background

Currently there are limited networking options on the Akash network, we cannot create networks accross providers, so this limits how we can architecture in highly available services. Effectively you need to consider your services akin to serverless, in that you are limited to your pod, thus usermode means you cannot do typical networking. So our goal was to find a way to create our overlay network within these constraints. We are pleased to present an active active database service running accross two providers.

- [Demo Video](https://ody.sh/jYN7U46grF)
- [Source Code for Demo CockRoachDB APP](https://github.com/Cypherpunk-Labs/akash-demo-app-cockroachdb)

# User stories

## As a web admin I want to add resiliency to my site, so I need to replicate my backend services without over exposing my service to the public internet.

# Outcome

- Write a guide on how to integrate east west networking for cross provider high availability leveraging a two tiered application with backend replication.  

# Workstream

### Tasks

- [x] Test Wireguard > FAILED > will not run, needs to insert kernel module.
- [x] Test Tailscale > SUCCESS > needs testing if it will run in akash (no marketplace sdls). REF:https://tailscale.com/kb/1108/cloudrun/
  - [x] magic dns works in pod once nameserver 100.100.100.100 is added to /etc/resolv.conf (known full/short host name can be used by services to replicate/cluster).
- [x] Create Demos
  - [x] create sdl bundle to demo, 
  - [ ] leverage confidential container to protect the key.
  - [x] create video demo
- [ ] Research if we think an encryption key escrow is worth the effort thus add as provider feature we can sidecar in, or leave bundling binaries etc to user task.
- [ ] Research consul
- [ ] [Incorporate cell based architecture](https://github.com/wso2/reference-architecture/blob/master/reference-architecture-cell-based.md)
