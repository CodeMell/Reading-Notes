# CRUD

## [Status Codes Based On REST Methods]()

1. In your own words, describe what each group of status code represents:

    - 100’s = tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client

    - 200’s = tell the client that its request was accepted

    - 300’s = tell the client that the resource they are requesting isn’t available at the expected location anymore

    - 400’s = about invalid requests a client sent to a server
    - 500’s =

2. What is a status code 202?
    -  Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.

3. What is a status code 308?
    - Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.
    
4. What code would you use if an update didn’t return data to a client?
    - 204 No Content

5. What code would you use if a resource used to exist but no longer does?
    - 410 Gone

6. What is the ‘Forbidden’ status code?
    - 403 Forbidden


## [Build A REST API With Node.js, Express, & MongoDB - Quick]() - First 20 minutes

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
    - 

2. What is middleware?
    - software and cloud services that provide common services and capabilities to applications and help developers and operators build and deploy applications more efficiently.

3. What does app.use(express.json()) do?
    - It parses incoming requests with JSON payloads and puts the parsed data in req.body.

4. What does the /:id mean in a route?
    -  a unique identifier assigned to every order that is protected by Route Package Protection.

5. What is the difference between PUT and PATCH?
    - PUT  is used to set an entity's information completely. PUTting is similar to POSTing, except that it will overwrite the entity if already exists or create it otherwise. You could use a PUT to write a user to your database that may already be in it. While PATCH is used to update an existing entity with new information. You can't patch an entity that doesn't exist. 

6. How do you make a default value in a schema?
    - 

7. What does a 500 error status code mean?
    -  the server encountered an unexpected condition that prevented it from fulfilling the request.

8. What is the difference between a status 200 and a status 201?
    - Status 201 mean the request has succeeded and has led to the creation of a resource. Status 200 mean the code that is delivered when a web page or resource acts exactly the way it's expected to.

    ## Things I want to know more about
