# kubernetes-ingress-project

This is based on volume concept

Kubernetes will create a separate volume which will have all the data of an node & when the node is deleted it will store all the data at the location which have been set as mount point.

Here we have mount point as /mnt/data

When we add some data to mount point location, it will get added to pods which will get created

Steps -
First create all the yaml files on visual code.

Than push it to github repository.

Use killercoda or EKS for deployement of code.

Open killercoda - Kubernetes

kubectl get pods(no pods are present)

kubectl get nodes(there will be one node & one master node running)

git clone https://github.com/Username/repositoryname.git

![image](https://github.com/Rinki-shrivastava/kubernetes-ingress-project/assets/153551978/b06961b4-89c6-401b-a9b3-f999ebc26561)

cd kubernetes-ingress-project

ls

kubectl apply -f pv.yaml

kubectl apply -f claim.yaml

kubectl apply -f pod1.yaml

kubectl get pods

kubeclt get pods -o wide

curl 192.168.1.4 (page will get hit)

![image](https://github.com/Rinki-shrivastava/kubernetes-ingress-project/assets/153551978/74960eb7-50d7-48d0-933c-4d2a04c22681)

Now create the mount path directory on local machine

cd /mnt

ls

mkdir data

ls

cd

cd kubernetes-ingress-project

kubectl exec -it pod1 bash (you will get entered in container)

cd htdocs

cat > index.html (add some data & exit from it)

curl 192.168.1.4 (updated data will be shown to you)

![image](https://github.com/Rinki-shrivastava/kubernetes-ingress-project/assets/153551978/3cbefd1a-6cda-4124-af40-7ffa6bfb2c05)

kubectl get pods (only we have one pod)

create another pod this will also have the same data

kubectl apply -f pod2.yaml

![image](https://github.com/Rinki-shrivastava/kubernetes-ingress-project/assets/153551978/c66c48e9-5b03-4c49-8375-3a34e1924f13)

