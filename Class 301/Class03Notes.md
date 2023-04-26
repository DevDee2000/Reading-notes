# Lists and Keys in React <hr>


### <ins>**Rendering Multiple Components**</ins>

- You can build collections of elements and include them in JSX using curly braces {}.

- Below, we loop through the numbers array using the JavaScript map() function. We return a < li > element for each item. Finally, we assign the resulting array of elements to listItems:

![](/read03%20exapmle%201.png)

- Then, we can include the entire listItems array inside a <ul> element:

![](/read03%20example%202.png)

### <ins>**Basic List Component**</ins>

- Usually you would render lists inside a component.

- We can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.


## <ins>**The Spread Operator**</ins>

- The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function's arguments

### <ins>?**What is the spread operator?**</ins>?

- In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.


Here are some other things that the spread operator can do.

- Copying an array

- Concatenating or combining arrays

- Using Math functions

- Using an array as arguments

- Adding an item to a list

- Adding to state in React

- Combining objects

- Converting NodeList to an array

In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any iterable, including a string

- Here are a couple basic examples of using … in JavaScript, where I demonstrate copying an array, splitting a string into characters, and combining the properties of two JavaScript objects:

![](/Screenshot%202023-04-25%20at%2010.21.31%20AM.png)











## <ins>React Docs - lists and keys Questions</ins>

- Q. What does .map() return?


- A. The .map() method returns a new array that contains the results of calling a provided function on each element of the original array. This means that the method does not modify the original array, but instead creates a new array based on the transformation performed by the provided function.



- Q.If I want to loop through an array and display each value in JSX, how do I do that in React?


- A. By using the .map() method to loop through the array and display the numbers


- Q.Each list item needs a unique ____.


- A. key

- Q.What is the purpose of a key?


- A. In React, the key is a special attribute that is used to identify which items in a list of components have changed, been added or removed.

&nbsp;

## The Spread Operator

- Q. What is the spread operator?


- A. The spread operator is a feature in programming languages that allows an iterable, such as an array or an object, to be expanded into individual elements.

- Q. List 4 things that the spread operator can do.


- A. Copying an array
-   Concatenating or combining arrays
-   Using Math functions
-   Using an array as arguments
  
- Q. Give an example of using the spread operator to combine two arrays.


- A.   const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const combinedArr = [...arr1, ...arr2];

console.log(combinedArr); // [1, 2, 3, 4, 5, 6]






- Q. Give an example of using the spread operator to add a new item to an array.


- A.  const numbers = [1, 2, 3];
const newNumber = 4;

const newArray = [...numbers, newNumber];

console.log(newArray); // Output: [1, 2, 3, 4]


- Q. Give an example of using the spread operator to combine two objects into one.


- A. const object1 = { x: 1, y: 2 };
const object2 = { z: 3, w: 4 };

const combinedObject = { ...object1, ...object2 };

console.log(combinedObject); // Output: { x: 1, y: 2, z: 3, w: 4 }


### 

- Q. In the video, what is the first step that the developer does to pass functions between components?


- A.

- Q. In your own words, what does the increment function do?


- A.

- Q. How can you pass a method from a parent component into a child component?


- A.

- Q. How does the child component invoke a method that was passed to it from a parent component?


- A.

















## Things I want to know more about