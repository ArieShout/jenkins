# Initial Setup for AKS Blue/Green Deployment

To setup the deployment target to another AKS, apply the `resources.yml` to that AKS:

```sh
kubectl apply -f resources.yml
```

Then, update the `resourceGroup` and `aks` the pipeline script in the blue/green deployment Job:

```groovy
node {
    def resourceGroup = '<your-resource-group>'
    def aks = '<your-aks-name>'
    
    ...
    
}
```
