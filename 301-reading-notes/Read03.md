### Lists and Keys

First, let’s review how you transform lists in JavaScript.

Given the code below, we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it:

### Rendering Multiple Components

You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a (li) element for each item. Finally, we assign the resulting array of elements to listItems

### Basic List Component

Usually you would render lists inside a component.

We can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.

When you run this code, you’ll be given a warning that a key should be provided for list items. A “key” is a special string attribute you need to include when creating lists of elements. We’ll discuss why it’s important in the next section.

Let’s assign a key to our list items inside numbers.map() and fix the missing key issue.

### Keys
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity:

The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys:

When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort:

### Extracting Components with Keys

Keys only make sense in the context of the surrounding array."

For example, if you extract a ListItem component, you should keep the key on the (ListItem ) elements in the array rather than on the (li) element in the ListItem itself.

## How to Use the Spread Operator (…) in JavaScript

The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

### What is the spread operator?

InJavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

“When ...arr is used in the function call, it ‘expands’ an iterable object arr into the list of arguments.” — JavaScript.info

The spread operator was added to JavaScript in ES6 (ES2015), just like the rest parameters, which have the same syntax: three magic dots …

### What is ... used for?

“Spread operator to the rescue! It looks similar to rest parameters, also using ..., but does quite the opposite.” — JavaScript.info

+ Copying an array
+ 
+ Concatenating or combining arrays
+ 
+ Using Math functions
+ 
+ Using an array as arguments
+ 
+ Adding an item to a list
+ 
+ Adding to state in React
+ 
+ Combining objects
+ 
+ Converting NodeList to an array

+ In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string.
