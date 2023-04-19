# ***React Lifecycle*** <hr>

## <ins>**What are component lifecycle events?**</ins>

- <p>React lets you define components as classes or functions. The methods that you are able to use on these are called lifecycle events. These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.</p>

- <p>Mounting, Updating, and Unmounting are the three phases of the component lifecycle.</p>

### <ins>**Mounting**</ins>

- <p>When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.</p>

- Q. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

- A. Render occurs before componentDidMount

- Q. What is the very first thing to happen in the lifecycle of React?

-A. Mounting is the first thing that happens in the lifecycle

- Q. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

- A. constructor, render, componentDidMount, React Updates, componentWillUnmount

- Q. What does componentDidMount do?

- A.  If you need to load anything using a network request or initialize the DOM, it should go here.

- Q. What types of things can you pass in the props?

- A. 

- Q. What is the big difference between props and state?

- A. props pass into a component and state is handled inside of that component and can be updated in that component as well. props are handled outside of the component

- Q.When do we re-render our application?

- A. When we are changing the state inside of the application

- Q. What are some examples of things that we could store in state?

- A. checkboxes, inputs, forms, and anything else that will change as the user continues to use the application.