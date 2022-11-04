# Vagrant, K3s and 3 little web applications

In this second part of the project, we will configure 3 little webapp under k3s.

The `Vagrantfile` will create a k3s cluster with a single node and copy the `kubectl` config file at the root of the folder.

You can use that file with:

```bash
kubectl --kubeconfig kubectl.config.yml ...
```

or by setting the env variable

```bash
export KUBECONFIG=$(pwd)/kubectl.config.yml
kubectl ...
```
