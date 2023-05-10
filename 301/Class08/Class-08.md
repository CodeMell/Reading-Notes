# APIs

[API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

1. What does REST stand for?
    - Roy Fielding proposed Representational State Transfer

2. REST APIs are designed around a ____.
    - resources (any kind of object, data, or service that can be accessed by the client)

3. What is an identifier of a resource? Give an example.
    -  URI that uniquely identifies that resource
    example: https://adventure-works.com/orders/1

4. What are the most common HTTP verbs?
    - GET, POST, PUT, PATCH, and DELETE.

5. What should the URIs be based on?
    - on nouns (the resource)

6. Give an example of a good URI.
    - /customers is the path to the customers collection, and /customers/5 is the path to the customer with ID equal to 5

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    -  expose a large number of small resources
    
8. What status code does a successful GET request return?
    - returns a status code of 200

9. What status code does an unsuccessful GET request return?
    - returns a status code of 404

10. What status code does a successful POST request return?
    - returns a status code of 201 

11. What status code does a successful DELETE request return?
    - returns a status code of 204


## Bookmark and Review
[RegExr](https://regexr.com/) - Pay particular attention to the cheatsheet
[Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
[Regex 101](https://regex101.com/)

## Things I want to know more about