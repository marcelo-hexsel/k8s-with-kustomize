# K8s with Kustomize

The main objective is to manage diferent pods based on the same image, but with different replicas count and environment variables (via configmaps).  
In this sample, we have a base nginx deployment, wich is used as a base for two other "kustomizations".

## Requirements

You will need a kubernetes cluster and ```kubectl``` installed

## How to run

To show the result of nginx-one deployment and configurations:
```
kubectl kustomize ./overlays/one/
```

To show the result of nginx-two deployment and configurations:
```
kubectl kustomize ./overlays/one/
```

To apply deployment and configuration for nginx-one, for instance:
```
kubectl apply -k ./overlays/one/
```

## Conclusion

If you check the cluster after applying kustomizations, you should see different deployments/replicas/configmaps/environment-variables for each variant
