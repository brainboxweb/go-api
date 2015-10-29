
The basis for this code is the following article:

* <https://medium.com/@etiennerouzeaud/how-to-create-a-basic-restful-api-in-go-c8e032ba3181#.65f3rzrge>
        

Dependencies
---

        go get github.com/gin-gonic/gin
        go get gopkg.in/gorp.v1
        go get github.com/mattn/go-sqlite3


Run
---

        go run main.go
        
        
Test
----
        //list
        curl http://localhost:8080/api/v1/users
        //[]
         
        //add 
        curl -i -X POST -H "Content-Type: application/json" -d "{ \"firstname\": \"Thea\", \"lastname\": \"Queen\" }" http://localhost:8080/api/v1/users
         
        //list
        curl http://localhost:8080/api/v1/users
        //[{"id":1,"firstname":"Thea","lastname":"Queen"}]
         
        //update
        curl -i -X PUT -H "Content-Type: application/json" -d "{ \"firstname\": \"Thea\", \"lastname\": \"Merlyn\" }" http://localhost:8080/api/v1/users/1
     
        //list
        curl http://localhost:8080/api/v1/users
        //[{"id":1,"firstname":"Thea","lastname":"Merlyn"}]
        
        //delete
        curl -i -X DELETE http://localhost:8080/api/v1/users/1
        
        //list
        curl http://localhost:8080/api/v1/users
        //[]
        