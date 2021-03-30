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
<a href="https://github.com/Quan25/kubernetes_project/blob/master/CS571_Signature_Project_Quan_Zhou.pdf"> document</a>
</details>

#### Sample Output ####

- Access a student's score
```
curl cs571.project.com/studentserver/api/score?student_id=11111
```

- List all the books
```curl cs571.project.com/bookshelf/books```


- Add a book
```curl -X POST -d "{\"book_name\": \"cloud computing\",\"book_author\": \"unkown\", \"isbn\": \"123456\" }" http://cs571.project.com/bookshelf/book```




- Update a book
```curl -X PUT -d "{\"book_name\": \"123\",\"book_author\": \"test\", \"isbn\": \"123updated\" }" http://cs571.project.com/bookshelf/book/id```




- Delete a book
```curl -X DELETE cs571.project.com/bookshelf/book/id```
