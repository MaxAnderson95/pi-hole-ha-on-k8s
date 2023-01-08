# HA Pi-hole on K8s

This code accompanies a blog post on my website. [Head over there](https://maxanderson.tech/posts/pi-hole-ha-on-k8s/) for all of the details.

## Pre-requisites

- A way to expose Services of type LoadBalancer. In my cluster I utilize MetalLB.
- An ingress controller. I’m using Traefik and subsequently will be using Traefik’s custom IngressRoute CRD. But it can easily be adapted to use a standard Ingress definition.
- CertManager to issue certificates for the web interface.
- A persistent volume storage system with auto-provisioning. I’m using Longhorn

## Install

```
kubectl apply -f ./manifests
```
