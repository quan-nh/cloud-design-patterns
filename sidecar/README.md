# Sidecar Pattern

<img src="http://turnoff.us/image/en/depressed-developer-52.png" width="500">

[Sidecar pattern
](https://docs.microsoft.com/en-us/azure/architecture/patterns/sidecar)

## Use Case

- [Log aggregator sidecar pattern
](https://cloud.google.com/solutions/best-practices-for-operating-containers#log_aggregator_sidecar_pattern)

## Sample

- Create GKE cluster & connect to it.

- Deploy
```sh
# keycloak
$ kubectl create configmap keycloak-config --from-file=keycloak-sample-realm.json
$ kubectl apply -f keycloak-deployment.yaml

$ kubectl get services
```
