This is an example of a kubernetes pod created with a separate configuration yaml file and a separate secret yaml file.

To run:
From the config_and_secret directory run the apply command on the configuration yaml
```
kubectl apply -f basic-configuration.yaml
```

Then run the apply command on the secret yaml:
```
kubectl apply -f basic-secret.yaml
```

Then run the apply command on the working_pod_with_no_serviceAccount yaml:
```
kubectl apply -f working_pod_with_no_serviceAccount.yaml
```

Check your pod:
```
kubectl get pods
kubectl describe pod pod-for-config-secret
``` 
