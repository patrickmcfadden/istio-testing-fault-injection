# Automated Error Tests

This is an example repository for showing how you can use your pipeline to orchestrate error case tests and build a more resilient application


## Deploy the application

*Assumptions:*
* You have a kubernetes cluster
* Istio is installed with:
  *  ingress-gateway
  * default namespace is labeled for auto-injection of the sidecar
```
kubectl apply -f manifests
```

### Running tests

`npm test`

### Checking error cases

```
kubectl apply -f manifest-errors
npm run test-error
```