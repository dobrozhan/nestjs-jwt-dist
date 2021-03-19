To start build, simply use 

npm start

Token for API test

JWT = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImtlZXAiLCJlbWFpbCI6ImRvYnJvemhhbi5hQGdtYWlsLmNvbSIsImlhdCI6MTYxNjE0MTgxOSwiZXhwIjoxNjE2NzQ2NjE5fQ.Gt0GP9MutUoGm0K_b_IZN38O2wUIqHvOxHre984amnE'


In case, you need to generate JWT and perform  API test on this project, please follow the next steps


a) Using predefined JWT

   curl http://localhost:3000/auth/google -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImtlZXAiLCJlbWFpbCI6ImRvYnJvemhhbi5hQGdtYWlsLmNvbSIsImlhdCI6MTYxNjE0MTgxOSwiZXhwIjoxNjE2NzQ2NjE5fQ.Gt0GP9MutUoGm0K_b_IZN38O2wUIqHvOxHre984amnE"


b) Using new JWT  
 - Authorize user (note: user hard coded in users/users.service.ts)
    
   curl -X POST http://localhost:3000/auth/login -d '{"username": "keep", "password": "secret"}' -H "Content-Type: application/json"   
        
 - As a result, you will get new token (NewJWT), use it for the next request
   
   curl http://localhost:3000/auth/google -H "Authorization: Bearer NewJWT"
   
    I hope you will find it effective.
    Best, 
    OD
