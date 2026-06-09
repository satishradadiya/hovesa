# GKE Kubernetes Manifests

This directory contains a clean, organized set of Kubernetes manifests for deploying the Hovesa stack on GKE.

## Structure

- `namespace.yaml` - dedicated namespace for the app
- `configmap.yaml` - non-sensitive configuration
- `secrets.example.yaml` - example secrets template
- `mysql.yaml` - MariaDB deployment + service + persistent storage
- `redis.yaml` - Redis deployment + service + persistent storage
- `litespeed.yaml` - OpenLiteSpeed deployment + service + ingress-ready ports
- `kustomization.yaml` - simple assembly entrypoint for `kubectl apply -k`

## Notes

- Replace placeholder values in `secrets.example.yaml` with real credentials.
- For production GKE, consider using managed services for MySQL and Redis.
- Persistent volumes here are represented with standard PVCs so they can bind to GKE storage classes.
