# Sidecar Pattern

<img src="http://turnoff.us/image/en/depressed-developer-52.png" width="500">

[Sidecar pattern
](https://docs.microsoft.com/en-us/azure/architecture/patterns/sidecar)

## Use Case

- [Log aggregator sidecar pattern
](https://cloud.google.com/solutions/best-practices-for-operating-containers#log_aggregator_sidecar_pattern)

## Sample

<img src="https://miro.medium.com/max/1400/0*L6GAQ_uhKQGRVzcH" width="600">

- Create GKE cluster & connect to it.

- Deploy
```sh
# keycloak
$ kubectl create configmap keycloak-config --from-file=keycloak-sample-realm.json
$ kubectl apply -f keycloak-deployment.yaml

# app-with-sidecar
$ gcloud builds submit -t gcr.io/bookshelf-project-240508/clj-web clj-web/
$ kubectl create configmap gatekeeper-config --from-file=keycloak-gatekeeper.yaml
$ kubectl apply -f app-deployment.yaml

$ kubectl get services
$ kubectl get pods
$ kubectl logs app-with-sidecar-xx -c sidecar-container --follow
```
