## Instructions

1. Create a file named `pi-pod.yaml` with the content included in this directory:


2. Apply the YAML to create the pod:

    kubectl apply -f pi-pod.yaml


3. Wait for the pod to finish running. You can check the pod status with:

    kubectl get pod pi

    The pod is ready when the status shows `Completed`.

4. Once the pod has completed, retrieve the logs and save them locally:

    kubectl logs pi > $(pwd)/pi-logs.txt

5. Verify the contents of the log file:

    cat pi-logs.txt

6. (Optional) To clean up the pod, run:

    kubectl delete pod pi

