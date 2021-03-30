# kubernetes_project
This project uses the following techniques

Techniques           | Usage
-------------------- | ---------------------
Pods                 | to run 2 applications
Service              | for outside access the application
Persistence Volumes  | to store the data with MongoDB
Ingress              | to expose both applications under same domain but different path
ConfigMaps           | to store MongoDB service address, in case MongoDB is down and restarts with a different service address, and with ConfigMaps, we don't need to build the docker image again with the new address
 ---
#### Pod 1: student records ####
Node.js webserver that allows users to access certain student record from given student_id.
#### Pod 2: bookstore ####
MongoDB + Python Flask Web Framework + REST API + GKE
 ---
 ---
 ----

curl cs571.project.com/studentserver/api/score?student_id=11111
Pod 2: bookstore
curl cs571.project.com/bookshelf/books
ConfigMaps ----
