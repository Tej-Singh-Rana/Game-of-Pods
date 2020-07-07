### Pento Broken Server

> Note: -

1. At location of `/etc/kubernetes/manifests`, in kube-apiserver.yaml CA authority certificate name is wrong. Fix it with correct name.
2. Move into the path of `/root/.kube/`, as per description match the name of User and api-server Port number.
3. After cluster up, do `kubectl get nodes` to check the status of Nodes.
4. Second Node is not set to schedule Pods. Fix it with certain command. 
```
kubectl uncordon node01
```
5. Check the coredns Pods, in the kube-system namespace.
6. Edit the coredns deployment manifest file and insert image name as per description.
```
kubectl edit deploy coredns -n kube-system

kubectl get deploy coredns -n kube-system

kubectl get pods -n kube-system
```
7. Now cluster in configured to perform following tasks.
