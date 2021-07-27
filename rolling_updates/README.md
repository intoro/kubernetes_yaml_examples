# Rolling Updates
To use the rolling update feature start with a deploymet like in nginx_deployment.yaml 

Start the deployment:
```
kubectl apply -f nginx_deployment.yaml
```

Check the status of the deployment:
```
kubectl get all
```

Once the deployment is up and running use the set command to deploy a rollout to update the image of the nginx-pod pods of the deployment:
```
kubectl set image deployment/nginx-deployment nginx-pod=nginx:3 --record
```

Check the rollout status:
```
kubectl rollout status deployment/nginx-deployment
```

The rollout will never finish because the image provided does not exist. So ctrl-c and run the get all command. You will see three containers now, one not running. This is the new pod created by the rollout.

To roll back first check the rollout history:
```
kubectl rollout history deployment/nginx-deployment
```

Then undo the last rollout revision:
```
kubectl rollout undo deployment/nginx-deployment
```

Check the status:
```
kubectl get all
```

Running the status command again should now give a success message:
```
kubectl rollout status deployment/nginx-deployment
```
