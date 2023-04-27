# ***Forms*** <hr>

HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state.


This form has the default HTML form behavior of browsing to a new page when the user submits the form. If you want this behavior in React, it just works. But in most cases, it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form. The standard way to achieve this is with a technique called “controlled components”.

    
### Control Components 

- In HTML, form elements such as < input>, < textarea>, and < select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().


- We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.


- Q. What is a ‘Controlled Component’?


- A. a controlled component is a component that is fully controlled by the application's logic rather than the component itself.


- Q. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.


- A. update their responses as soon as they enter them. It gives the user a better experience and allows them to make corrections as they go. You minimalize the risk of data loss and it's also easier to keep track of changes. 


- Q. How do we target what the user is entering if we have an event handler on an input field?


- A. you would have to use event.target.value in order to target what the user enters.


- Q. Why would we use a ternary operator?


- A. to replace long if statements and to keep our code as dry as possible


- Q. Rewrite the following statement using a ternary statement:

![](/Read%2004%20question%20example.png)

- A.  x===y ? console.log(true) : console.log(false)

