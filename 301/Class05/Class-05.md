# Putting it all together
[React Docs - Thinking in React](https://reactjs.org/docs/thinking-in-react.html)
1. What is the single responsibility principle and how does it apply to components?
    - single-responsibility principle is a computer programming principle that states that "A module should be responsible to one, and only one, actor.

2. What does it mean to build a ‘static’ version of your application?
    -  a version that renders the UI from your data model without adding any interactivity

3. Once you have a static application, what do you need to add?
    - add interactivity

4. What are the three questions you can ask to determine if something is state?
    - Does it remain unchanged over time? If so, it isn’t state.
    Is it passed in from a parent via props? If so, it isn’t state.
    Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

5. How can you identify where state needs to live?
    - Often, you can put the state directly into their common parent.
    You can also put the state into some component above their common parent.
    If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

[Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)
1. What is a “higher-order function”?
    - Functions that operate on other functions, either by taking them as arguments or by returning them

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
    
            function greaterThan(n) {
            return m => m > n;
            }
            let greaterThan10 = greaterThan(10);
            console.log(greaterThan10(11));
            // → true
    -The function is comparing the variables and anything that is greater than n will be true and less than n will be false

    - line two of the function is returning m as it being greater than n

3. Explain how either map or reduce operates, with regards to higher-order functions.
    - Reduce computes a single value from an array. it builds a value by repeatedly taking a single element from the array and combining it with the current value when it comes to higher order operations

## Things I want to know more about