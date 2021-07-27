Find the broken pods:
```
kubectl get pods --all-namespaces
```
Check the STATUS field to find the broken pod.

You can also view the resource usage for all pods:
```
kubectl  top pod -n <namespace>
```

Use the describe command to get a pods details:
```
kubectl describe pod <pod_name> -n <namespace>
```

You can send a pods data to a file with the -o argument:
```
kubectl get pod <pod_name> -n <namespace> -o json > /home/folder/pod-details.json
```

You can do the same for container logs:
```
kubectl logs <pod_name> -n <namespace> > /home/folder/pod-logs.log
```
