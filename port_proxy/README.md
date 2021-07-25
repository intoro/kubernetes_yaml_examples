To start the pods:
```
kubectl apply -f haproxy-config.yaml
kubectl apply -f 2-container-pod.yaml
kubectl apply -f busybox-to-test-proxy.yaml
```

to run the test:
```
kubectl exec busybox -- curl $(kubectl get pod give-fruit-service -o=custom-columns=IP:.status.podIP --no-headers):80
```



