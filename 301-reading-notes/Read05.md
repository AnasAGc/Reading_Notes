# Thinking in React


## Staps to built React applications :  

###  1-Break The UI Into A Component Hierarchy:

to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

###  2-Build A Static Version in React:

to implement your app.

###  3-Identify The Minimal (but complete) Representation Of UI State:

to be able to trigger changes to your underlying data model. React achieves this with state.

### 4- Identify Where Your State Should Live:

to identify which component mutates, or owns, this state.

### 5-Add Inverse Data Flow:

to support data flowing the other way: the form components deep in the hierarchy need to update the state in FilterableProductTable.


## Questions:

### Q1:How would you break a mock into a component heirarchy?

 by putting each separate each component and pass the data between them using the props and state

 ### Q2:What is the single responsibility principle and how does it apply to components?

 a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents

 ### Q3:What does it mean to build a ‘static’ version of your application?

 by building mock that consists of components that reuse other components and pass data using props and never use the state.

 ### Q4:Once you have a static application, what do you need to add?

after that you need to make the UI interactive. and this can be done by using the state to trigger changes.

 ### Q5:What are the three questions you can ask to determine if something is state?

+ Is it passed in from a parent via props? If so, it probably isn’t state.

+ Does it remain unchanged over time? If so, it probably isn’t state.

+ Can you compute it based on any other state or props in your component? If so, it isn’t state.

 ### Q6:How can you identify where state needs to live?

+ Identify every component that renders something based on that state.

+ Find a common owner component (a single component above all the components that need the state in the hierarchy).

+ Either the common owner or another component higher up in the hierarchy should own the state.

+ If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
