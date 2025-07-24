Use the following command to install Metric Server:
kubectl apply -f https://raw.githubusercontent.com/pythianarora/total-practice/master/sample-kubernetes-code/metrics-server.yaml

Ensure that metrics was properly installed and working properly by running:
kubectl top pods --all-namespaces

run the following command to find the pod with the highest CPU usage across all name spaces and redirect the results to a .txt file:
kubectl top pods --all-namespaces --no-headers | sort -k3 -nr | head -n 1 | awk '{print $2}' > /data/cpu/most.txt

check the .txt file to ensure that data was properly transfered 

Use the following command to remove Metrics Server from your cluster:
kubectl delete -f https://raw.githubusercontent.com/pythianarora/total-practice/master/sample-kubernetes-code/metrics-server.yaml

