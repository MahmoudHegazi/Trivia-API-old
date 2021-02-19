# Python-API

# Introduction:

* The Triva is Python API Not Rect app organized around REST. Our API has predictable resource-oriented URLs, accepts form-encoded request bodies, returns JSON-encoded responses, and uses standard HTTP response codes.
* you can use this API TO create, read , questions there are 6 cateogries and you can play question game and searck for a question this is A python API not any other thing Like this Lesson Name API
* get full pagination list of the questions 


## how to set up the local development for FLASK API

* npm install only once to install dependency 
* npm start
* on Windows: Download GitBash, open it, ```cd [project_folder]``` run these 3 commands 
* ``` export FLASK_APP=flaskr ```
* ``` export FLASK_ENV=development ```
* ``` flask run ```
* For Linux users, you can use the same three commands to start the API

# Errors:
* Your Library API May return 4 types of errors [404, 422, 400, 405, 409]

### 404 Resource Not Found:

* example of the response : 
    ```json
       {
        'code':404,
        'message':'resource not found',
        'success':False
        }
    ```
    
### 422 Unprocessable:

* JSON response will return and this error happens if Your API request unprocessable That's mean The API received your request but it could not handle your request
* -- For example, if you delete a question that does not exist, 
* An example of a response: 
    ```json
       {
        'code':422,
        'message':'unprocessable',
        'success':False
        }
    ```
    
### 400 Bad Request:

* JSON response will return and this error happens if you send A bad request the API could not understand it 
* -- For example,  send Not JSON body to the POST / Patch endpoints,
* An example of a response: 
    ```json
       {
        'code':400,
        'message':'bad request',
        'success':False
        }
    ```
    
### 405 Method not allowed:
* It's an HTTP response status code that indicates that the request method is known by the server but is not supported by the target resource
* -- For example,  send post request to endpoint that accept only Patch or GET requests
* JSON response will return and this error happens if used A wrong Method in your request 

* An example of a response: 
    ```json
       {
        'code':405,
        'message':'method not allowed',
        'success':False
        }
    ```
    
    
### 409 conflict:
* It's an HTTP response status code returned when you try create a question that already exist

* An example of a response: 
    ```json
        {
        'code':409,
        'message':'the question cannot be added, because it already exists',
        'success':False
       }
    ``` 
    
    # GET All Questions [GET]
    * path: localhost:5000/questions
    
            * return all questions paginated list of the questions start from page 1 each page contains 10 questions 
    
    
    # POST New Questions  [POST]
    * path: localhost:5000/add  ||  localhost:5000/questions
    
        
    # DELETE Questions  [POST]
    * path: localhost:5000/questions/<question_id>
    
    # GET Questions By category ID  [GET]
    * path: http://localhost:5000/categories/<category_id>/questions
    
    # GET Questions By category type  [GET]
    * path: http://localhost:5000/categories/<category>/questions
    
    # Play Questions Game  [POST]
    * path: http://localhost:5000/play  || http://localhost:5000/quizzes
    
    
   
    
