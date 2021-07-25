## React and Forms

HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state. For example, this form in plain HTML accepts a single name:



```

  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>

```

This form has the default HTML form behavior of browsing to a new page when the user submits the form. If you want this behavior in React, it just works. But in most cases, it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form. The standard way to achieve this is with a technique called “controlled components”.


## Controlled Components


In HTML, form elements such as (input), (textarea), and (select) typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.


## Alternatives to Controlled Components

It can sometimes be tedious to use controlled components, because you need to write an event handler for every way your data can change and pipe all of the input state through a React component. This can become particularly annoying when you are converting a preexisting codebase to React, or integrating a React application with a non-React library. In these situations, you might want to check out uncontrolled components, an alternative technique for implementing input forms.



# JavaScript — The Conditional (Ternary) Operator Explained.

Why would we use a ternary operator?


beacuse it's shortened way of writing an if-else statement, by writing one line of code with three arguments, the condition, the result upon the true comparison, and the result upon the false comparison.

### Rewrite the following statement using a ternary statement:

````
if(x===y){
console.log(true);
} else {
console.log(false);
}
````


````
let result= ((x===y)? 'true': 'false');

````

