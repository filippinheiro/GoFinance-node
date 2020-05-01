# GoFinance API

---

Go Finance is a light, easy to use REST API to register your finance transactions (income and outcome), you can record your earnings and
expenses, divide them in categories, import pre-existent transactions files and list them intuitively with our endpoints

---
## Routes

  - `GET /transactions` - It will return all the transactions registered on the database (you can find the format in the api specs)
    
    - `POST /transactions` - Allows you to create a new transaction according to the specified format in the documentation
    
    - `DELETE /transactions/:id` - Allows you to delete a given transaction
    
    - `POST /transactions/import` - import a CSV file with the pre existent transactions and all of them will be read and 
      save to the database
      
---
    ## Techs
    
      - Node.JS
      - Typescript
      - Express.js
      - Postgres
      - TypeORM
      - Jest
      - multer
      
      For code style the eslint and prettier are both set for this projects
      
    ---
    
      ## Running
      
        In order to run this API locally you need to first create a database (We advice to use postgres as it was originallyu intended to)
       and configure the ormconfig.json file with the name, user and password (you can usa a docker container to do so)
       
       then run the following commands 
       
       ```
        yarn
        yarn typeorm migration:run
        
        ```
        
        With that done it's all set, you can run yarn dev:server and/or start working with the code already
