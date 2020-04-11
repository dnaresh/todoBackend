# todoBackend

## Getting Started

Basic TodoApp Backend Developed using NodeJs, MongoDB,ExpressJs,Redis,Websocket,Swagger,Postman. This is Project is for demo purpose.not use in production.

## Software Requirements
  All are latest versions.
  ```
  NodeJs 
  Mongo Db
  Redis
  
  ```

## How to install

### 1). Clone the project from github to your-project-folder


```
git clone https://github.com/dnaresh/todoBackend.git ./your-project-folder
```

### 2). Using manual download ZIP
      a). Download repository
      b). Uncompress to your-project-folder

```
cd your-project-folder
npm install
npm update
```

## How to run

   Running in development mode (lifting API server)
   ```
     npm run dev
   ```
   You will know server is running by checking the output of the command npm run dev
   ```
      ****************************
      *    Starting Server
      *    Port: 3000
      *    NODE_ENV: development
      *    Database: MongoDB
      *    DB Connection: OK
      ****************************
   ```

## For web socket notification page 
 please open browser tab and enter below url then you go the landing page. press F12 to go to console. there you can see notifications during Task creation.

```
http://localhost:3000
```
   

## For Swagger Ui
 please open browser tab and enter below url

```
http://localhost:3000/docs
```


## Postman API Collection 
 You can import the ```postman-collection.json``` file located in ```postman collection folder``` to Postman. To import, click the import button located and select postman-collection.json located within the postman collection folder.

Go to manage environments to create environments for development, production, etc. On each of the environments you create you will need to:



### Authenticate Users creation:

```
POST register -- created a new admin user with name,email, password fields. we can create as many as users.
POST login  -- Authenticate the registered users with email and password fields and generate the JWT token.
```

After a successfull login it generates new JWT token.Create a new key authToken and save the JWT.
Each time you make a request to the API it will send Authorization header with the token value in the request, you can check this on the headers of todos endpoints in the Postman-collection.

Create a second key server with the url of your server, for development mode use http://localhost:3000


### todos 

```
GET  todos -- Get all todos created by current logged in user.
POST todos  -- Create todo
GET  todos/id  -- get unique todo
POST   todos/complete  -- Update the boolean value to complete todo.
PATCH   todos/id  -- Update the todo
DELETE  todos/id -- delete the todo
```

## Authors

* **d naresh** - *Initial work* (https://github.com/dnaresh)

