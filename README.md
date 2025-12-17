#docker_k8s
===========
first: created 2 customized index.html files, one within each directory 
then: dockerfiles to copy the customized index.html into the nginx home page
then: built two images with names of app1_nginx and app2_nginx 
then: pushed it to dockerhub
then: created 2 containers from each image for testing and everything is going fine (screenshots attached)
                          ====================================================
- created a pvc in the same namespace for app1 => this created a pv automatically (reclaim policy is delete by default, i changed it to retain)

- created a NodePort service from app1
- created an initContainer within the deployment to check if the html file exists in the pv, if not it copies the file to it.
- enabled the minikube ingress addon to install the nginx ingress controller 
