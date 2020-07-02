# k8-wordpress-ingress-tls
-
#Create a ReplicaSet with 2 replicas, which runs WordPress
#And attach it to MySQL ReplicaSet on a Persistent Volume
#Expose WordPress through Ingress with TLS certificate installed on it

Steps:
1) kubectl create secret generic mysql-pass --from-literal=password=######## 
2) kubectl create -f ./k8-wordpress-ingress-tls-/
3) kubectl get services -o wide #to check services running and to get NodePort if not assigned
4) kubectl get nodes -o wide # and get one of the external IPs of one of the nodes
5) Paste the IP address:NodePort in the Browser.

*#kubectl create secret generic wordpress-secret  --from-literal=password=######## if needed.
