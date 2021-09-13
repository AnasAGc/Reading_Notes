# React

## Conditional Rendering 
Conditional rendering in React works the same way conditions work in JavaScript, you can use if statement to check condition to do action :
`if (< condition >) { < action >/>; }`

**Element Variables** used to store elements , to render any part of the component later 

### Inline If with Logical && Operator :
to embed expressions in JSX by you should wrapping them in curly braces. This includes the JavaScript logical && operator :
`{unreadMessages.length}`
`5+7-9`
`[].length`

Inline If-Else with Conditional Operator Syntax :
`condition ? <action if condition true> : <action if condition false>`
Example :
` {isLoggedIn ? 'currently' : 'not'} `

**Preventing Component from Rendering**
To hidden any component based on special cases you should return null in the component function :

`if (!props.warn) { return null; } `

**Lists and Keys**
In React we use map to loop in the list items :

### Rendering Multiple Components
To render lists inside a component you need to create a list function loop in the list to get all item and return them , then you can use this function as component

Keys used to identify which items have changed, are added, or are removed , extracting components with Keys help us to modify the components later .

## Forms
Controlled Components are used to handles the submission of the form and has access to the data that the user entered into the form 

\<textarea\> is a HTML element defines its text by its children
\<select\> used to creates a drop-down list like un order list
\<input type="file"\> used to choose one or more files from the device storage to be uploaded to a server or manipulated by JavaScript by the File API.
name attribute : used to handle multiple controlled input elements

# Composition vs Inheritance
you should use the special children prop to pass children elements directly into their output on components that  don’t know their children

Specialization used for components that being “special cases” of other components , where a more “specific” component renders a more “generic” one 
If you want to reuse non-UI functionality between components,  import the function and use that function
