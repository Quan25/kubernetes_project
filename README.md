# kubernetes_project
This project uses the following techniques and runs on Google Kubernetes Engine

Techniques           | Usage
-------------------- | ---------------------
Pods                 | to run 2 applications
Service              | for outside access the application
Persistence Volumes  | to store the data with MongoDB
Ingress              | to expose both applications under same domain but different path
ConfigMaps           | to store MongoDB service address, in case MongoDB is down and restarts with a different service address, and with ConfigMaps, we don't need to build the docker image again with the new address
 ---
#### Pod 1: student records ####
- Node.js webserver that allows users to access certain student record from given student_id.
#### Pod 2: bookstore ####
- MongoDB + Python Flask Web Framework + REST API to allow users to perform standard List, Insert, Update, Delete operation to the data stored inside MongoDB

#### How to run ####
<details>
 <summary>Below is the document with detailed instruction</summary>
 <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
</details>
