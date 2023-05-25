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
    - 

3. What does app.use(express.json()) do?
    - 

4. What does the /:id mean in a route?
    - 

5. What is the difference between PUT and PATCH?
    - 

6. How do you make a default value in a schema?
    - 

7. What does a 500 error status code mean?
    - 

8. What is the difference between a status 200 and a status 201?
    - 

    ## Things I want to know more about
