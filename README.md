# kubernetes_yaml_examples
Examples of different deployments using kubernetes

Most examples can be run with the apply command:
```
kubectl apply -f <filename.yaml>
```

You can check the status of your pod with the get command:
```
kubectl get pods --all-namespaces
```

For a more in depth view of your pod use the describe command:
```
kubectl describe pod <pod name>
```

Use the delete command to remove the pod:
```
kubectl delete pod <pod name>
```
