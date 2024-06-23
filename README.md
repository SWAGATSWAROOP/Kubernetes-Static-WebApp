## todo-sql-app

A dynamic todo app deployed on Kubernetes cluster.

### How to run:

* Clone the repo
* ```kubectl create ns todo``` -- Create a namespace
* ```kubectl apply -f todo-sql-app/deploy/todo-v1.yaml``` -- Deploy the app
* ```stern todo``` -- Check the tail-logs
* ```kubectl port-forward todo-app-7cdfc755c-cq2g2 3000:3000``` -- Forward the port
* ```kubectl apply -f todo-sql-app/deploy/todo-service.yaml```
* ```kubectl get service todo```
* ```kubectl apply -f todo-sql-app/deploy/mysql-v1.yaml``` -- Deploy mysql
* ```stern mysql``` -- Check the tail-logs
* ```kubectl apply -f todo-sql-app/deploy/todo-v2.yaml``` -- Deploy the app with mysql






