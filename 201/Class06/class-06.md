# Problem Domain, Objects, and the DOM
[JavaScript Object Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
1. How would you describe an object to a non-technical friend you grew up with?
    An object is a collection of variables and functions.

2. What are some advantages to creating object literals?
    Sending a single object is much more efficient than sending several items individually, and it is easier to work with than an array, when you want to identify individual items by name.

3. How do objects differ from arrays?
    Instead of using an index number to select an item, you are using the name associated with each member's value.

4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
    You would need the name associaed with the value

5. Evaluate the code below. What does the term this refer to and what is the advantage to using this?

            const dog = {
            name: 'Spot',
            age: 2,
            color: 'white with black spots',
            humanAge: function (){
                console.log(`${this.name} is ${this.age*7} in human years`);
            }
            }

    this keyword refers to the current object the code is being written inside dog. Its enables you to use the same method definition for every object you create.


[Introduction To The DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
1. What is the DOM?
    The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web.

2. Briefly describe the relationship between the DOM and JavaScript.
    The DOM was designed to be independent of any particular programming language, making the structural representation of the document available from a single, consistent API.


## Bookmark and Review

[Understanding the problem domain is the hardest part of programming](http://simpleprogrammer.com/2013/07/15/understanding-the-problem-domain-is-the-hardest-part-of-programming)


[What’s the difference between primitive values and object references in JavaScript?](https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b)


## Things I want to know more about

