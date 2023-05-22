## In memory storage

## [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

1. What is a ‘call’?
    - a Manage function invocation

2. How many ‘calls’ can happen at once?
    - 1

3. What does LIFO mean?
    - Last In, First Out data structure

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
    - 
            function firstFunction(){
                console.log("Hello from firstFunction");
            }

            function secondFunction(){
            firstFunction();
            console.log("The end from secondFunction");
            }

            secondFunction();

5. What causes a Stack Overflow?
    - occurs when there is a recursive function (a function that calls itself) without an exit point

## [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

1. What is a ‘reference error’?
    - a variable that is not yet declared

2. What is a ‘syntax error’?
    - occurs when you have something that cannot be parsed in terms of syntax

3. What is a ‘range error’?
    - Try to manipulate an object with some kind of length and give it an invalid length

4. What is a ‘type error’?
    - when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable

5. What is a breakpoint?
    - a debugger statement in your code in the line

6. What does the word ‘debugger’ do in your code?
    - identifying coding errors at various stages of the operating system or application development

## Bookmark and Review
[JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

## Things I want to know more about