# kube-commands

## Accessing the application through the API server
```shell
 kubectl get --raw /api/v1/namespaces/default/pods/kiada/proxy/kiada
```
## Log container in kubernetes pod
```shell
kubectl logs kiada
```

## Streaming logs using kubectl logs -f
```
kubectl logs kiada -f
```
