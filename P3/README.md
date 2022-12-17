# K3d and Argo-CD

## Installation

Basically, you only need to do:

```shell
vagrant up
```

This will setup a VM:

- with `k3d + kubectl` configured.

    The provision will also create a file `kubectl.config.yml` that can be used
    by your local `kubectl` without ssh'ing into the VM.

- Create `k3d` cluster
- Install `argo-cd` on the cluster
- Start a service to access argocd web-ui at <https://192.168.56.110:9443>

## Connect to the argocd ui

To access argocd web-ui, goto <https://192.168.56.110:9443>

To login as admin, you need first to retrieve the generate password from argocd with the following command.

```shell
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
