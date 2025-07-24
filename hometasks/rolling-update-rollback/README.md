Run the following command in the same directory as the nginx-app.yaml file to create a namespace and apply a deployment inside that namespace:
kubectl apply -f nginx-app.yaml

The following command will trigger a rolling update to change the image to ngninx:latest:
kubectl set image deployment/nginx-app nginx=nginx:latest -n app-a

Verify that the rolling update was successfull:
kubectl rollout status deployment/nginx-app -n app-a

Use the following command to rollback the changes of the rolling update:
kubectl rollout undo deployment/nginx-app -n app-a