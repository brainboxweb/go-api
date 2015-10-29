Basis
---

        https://medium.com/@etiennerouzeaud/how-to-create-a-basic-restful-api-in-go-c8e032ba3181#.65f3rzrge
        
        
Run
---

        go run main.go
        
        
Test
----
         curl http://localhost:8080/api/v1/users
         //[{"id":1,"firstname":"Oliver","lastname":"Queen"},{"id":2,"firstname":"Malcom","lastname":"Merlyn"}]
         
         
         curl http://localhost:8080/api/v1/users/1
         //{"id":1,"firstname":"Oliver","lastname":"Queen"}
         
         curl http://localhost:8080/api/v1/users/2
         //{"id":2,"firstname":"Malcom","lastname":"Merlyn"}
         
         