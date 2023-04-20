# Passing Functions as Props
[React Docs - lists and keys](https://reactjs.org/docs/lists-and-keys.html)
1. What does .map() return?
    - array of numbers and double their values

2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    -  include them in JSX using curly braces {}

3. Each list item needs a unique ____.
    - key

4. What is the purpose of a key?
    - Help React identify which items have changed, are added, or are removed

[The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
1. What is the spread operator?
    - the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments

2. List 4 things that the spread operator can do.
    - Copying an array
    - Concatenating or combining arrays
    - Using Math functions
    - Using an array as arguments
    - Adding an item to a list
    - Adding to state in React
    - Combining objects
    - Converting NodeList to an array

3. Give an example of using the spread operator to combine two arrays. 

        [...["😋😛😜🤪😝"]] // Array [ "😋😛😜🤪😝" ]
        [..."🙂🙃😉😊😇🥰😍🤩!"] // Array(9) [ "🙂", "🙃", "😉", "😊", "😇", "🥰", "😍", "🤩", "!" ]
        const hello = {hello: "😋😛😜🤪😝"}
        const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}

        const helloWorld = {...hello,...world}
        console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" }


4. Give an example of using the spread operator to add a new item to an array.

             const fruits = ['🍏','🍊','🍌','🍉','🍍']
            const moreFruits = [...fruits];
            console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
            fruits[0] = '🍑'
            console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍


5. Give an example of using the spread operator to combine two objects into one.

        const myArray = [`🤪`,`🐻`,`🎌`]
        const yourArray = [`🙂`,`🤗`,`🤩`]
        const ourArray = [...myArray,...yourArray]
        console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩

[How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)
1. In the video, what is the first step that the developer does to pass functions between components?
    - 

2. In your own words, what does the increment function do?
    - 

3. How can you pass a method from a parent component into a child component?
    - 

4. How does the child component invoke a method that was passed to it from a parent component?
    - 

## Bookmark and Review
- [React Tutorial through ‘Declaring a Winner’](https://reactjs.org/tutorial/tutorial.html)
- [React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

## Things I want to know more about