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
```shell
kubectl logs kiada -f
```

## Displaying the timestamp of each logged line

```shell
kubectl logs kiada --timestamps=true
```

## Filter logs (recent)
```shell
kubectl logs kiada --since=25m
```
or
```shell
kubectl logs kiada --tail=5
```

## Run command in container running in Pod
```shell
kubectl exec kiada -- ps aux
```

## Running an interactive shell in container
```shell
 kubectl exec -it kiada -c kiada -- sh
```
or 
```shell
 kubectl exec -it kiada -c kiada -- bash
```
## Copy files from pod's container to host machine
```shell
kubectl  cp kiada:html/index.html /path/index.html -c kiada
```
## Copy files to pod's container 
```shell
kubectl cp /tmp/index.html kiada:html/ -c kiada
```
