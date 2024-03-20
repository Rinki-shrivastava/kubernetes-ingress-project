# kubernetes-ingress-project

This is based on volume concept
Kubernetes will create a separate volume which will have all the data of an node & when the node is deleted it will store all the data at the location which have been set as mount point.
Here we have mount point as /mnt/data
when we add some data to mount point location, it will get added to pods which will get created
