# Deploy Wiki.js on Kubernetes

## Requirements

 - [K8s cluster](https://kubernetes.io/docs/tasks/tools/)

## Deploy manifest to Kubernetes server

Download manifest:
````
git clone https://github.com/davma-io-templates/wikijs-template.git
cd wiki.js-template/kubernetes
````

Run the following command: 
````
kubectl apply -f wikijs.yaml
````

Check that it worked by running the following: 
````
kubectl port-forward service/wikijs-instance 3000:3000
````
Navigate to http://127.0.0.1:3000 in your browser. You should see a Wiki.js login page.
