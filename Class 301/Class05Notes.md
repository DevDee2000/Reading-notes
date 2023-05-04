# ***Thinking in React*** <hr>

## Step 1: Break the UI into a component hierarchy

Start by drawing boxes around every component and subcomponent in the mockup and naming them. If you work with a designer, they may have already named these components in their design tool.

Depending on your background, you can think about splitting up a design into components in different ways:

- Programming—use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

- CSS—consider what you would make class selectors for. (However, components are a bit less granular.)

- Design—consider how you would organize the design’s layers.


## Step 2: Build a static version in React

Now that you have your component hierarchy, it’s time to implement your app. The most straightforward approach is to build a version that renders the UI from your data model without adding any interactivity… yet! It’s often easier to build the static version first and add interactivity later. Building a static version requires a lot of typing and no thinking, but adding interactivity requires a lot of thinking and not a lot of typing.

- To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. Props are a way of passing data from parent to child. (If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.)

- You can either build “top down” by starting with building the components higher up in the hierarchy (like FilterableProductTable) or “bottom up” by working from components lower down (like ProductRow). In simpler examples, it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up.

- After building your components, you’ll have a library of reusable components that render your data model. Because this is a static app, the components will only return JSX. The component at the top of the hierarchy (FilterableProductTable) will take your data model as a prop. This is called one-way data flow because the data flows down from the top-level component to the ones at the bottom of the tree.

&nbsp;

## Step 3: Find the minimal but complete representation fo UI state

To make the UI interactive, you need to let users change your underlying data model. You will use state for this.

Think of state as the minimal set of changing data that your app needs to remember. The most important principle for structuring state is to keep it DRY (Don’t Repeat Yourself). Figure out the absolute minimal representation of the state your application needs and compute everything else on-demand. For example, if you’re building a shopping list, you can store the items as an array in state. If you want to also display the number of items in the list, don’t store the number of items as another state value—instead, read the length of your array.

Which of these are state? Identify the ones that are not:

- Does it remain unchanged over time? If so, it isn’t state.
- Is it passed in from a parent via props? If so, it isn’t state.
- Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

What’s left is probably state.

&nbsp;

## Step 4: Identify where your state should live.

After identifying your app’s minimal state data, you need to identify which component is responsible for changing this state, or owns the state. Remember: React uses one-way data flow, passing data down the component hierarchy from parent to child component. It may not be immediately clear which component should own what state. This can be challenging if you’re new to this concept, but you can figure it out by following these steps!

For each piece of state in your application:

1. Identify every component that renders something based on that state.
2. Find their closest common parent component—a component above them all in the hierarchy.
3. Decide where the state should live:
>1. Often, you can put the state directly into their common parent.

>>2. You can also put the state into some component above their common parent.
>>>3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

1 Q. What is the single responsibility principle and how does it apply to components?



- A. the idea that a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

&nbsp;

2 Q. What does it mean to build a ‘static’ version of your application?



- A. It means to build a version that renders the UI from your data model without adding any interactivity

&nbsp;

3 Q. Once you have a static application, what do you need to add?



- A. you need to add interactivity for the application

&nbsp;

4 Q. What are the three questions you can ask to determine if something is state?



- A.  Does it remain unchanged over time? If so, it isn’t state.
- Is it passed in from a parent via props? If so, it isn’t state.
- Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

&nbsp;

5 Q. How can you identify where state needs to live?



- A. Identify every component that renders something based on that state.
- Find their closest common parent component—a component above them all in the hierarchy.
- Decide where the state lives

&nbsp;

1 Q. What is a “higher-order function”?



- A. A higher-order function is a function that either takes one or more functions as arguments, or returns a function as its result

&nbsp;

2 Q. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?



- A. It's returning another function that checks to see if m is greater than n

&nbsp;

3 Q. Explain how either map or reduce operates, with regards to higher-order functions.



- A. The map method transforms an array by applying a function to all of its elements and building a new array from the returned values. The new array will have the same length as the input array, but its content will have been mapped to a new form by the function.



&nbsp;
