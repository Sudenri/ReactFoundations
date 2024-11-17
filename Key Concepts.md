# What is NextJs
Next.js is a flexible React framework that gives you building blocks to create fast, full-stack web applications.

Next.js is a React framework that gives you building blocks to create web applications.

By framework, we mean Next.js handles the tooling and configuration needed for React, and provides additional structure, features, and optimizations for your application.

You can use React to build your UI, then incrementally adopt Next.js features to solve common application requirements such as routing, data fetching, and caching - all while improving the developer and end-user experience.

# What is React
React is a JavaScript library for building interactive user interfaces.
By library, we mean React provides helpful functions (APIs) to build UI, but leaves it up to the developer where to use those functions in their application.

Part of React's success is that it is relatively unopinionated about the other aspects of building applications. This has resulted in a flourishing ecosystem of third-party tools and solutions, including Next.js.

It also means, however, that building a complete React application from the ground up requires some effort. Developers need to spend time configuring tools and reinventing solutions for common application requirements.

## DOM
The DOM is an object representation of the HTML elements. It acts as a bridge between your code and the user interface, and has a tree-like structure with parent and child relationships.

To use React in your newly created project, load two React scripts from an external website called unpkg.com:
react is the core React library.
react-dom provides DOM-specific methods that enable you to use React with the DOM.

##JSX
JSX is a syntax extension for JavaScript that allows you to describe your UI in a familiar HTML-like syntax. The nice thing about JSX is that apart from following three JSX rules, you don't need to learn any new symbols or syntax outside of HTML and JavaScript.
But browsers don't understand JSX out of the box, so you'll need a JavaScript compiler, such as a Babel, to transform your JSX code into regular JavaScript.

## Components
User interfaces can be broken down into smaller building blocks called components.

Components allow you to build self-contained, reusable snippets of code. If you think of components as LEGO bricks, you can take these individual bricks and combine them together to form larger structures. If you need to update a piece of the UI, you can update the specific component or brick.
* React components should be capitalized to distinguish them from plain HTML and JavaScript:
* you use React components the same way you'd use regular HTML tags, with angle brackets <>:

## Props
In the same way, you can pass pieces of information as properties to React components. These are called props. Take for instance, the possible variations of a button:
* To use the title prop, add curly braces {}. These are a special JSX syntax that allows you to write regular JavaScript directly inside your JSX markup.
* An object property with dot notation: `return <h1>{props.title}</h1>;`
* A Template literal: `return <h1>{`Cool ${title}`}</h1>;`
* Returned value of a function: `return <h1>{createTitle(title)}</h1>;`
* Ternary operator: `return <h1>{title ? title : 'Default Title'}</h1>;`

## Iterating through lists
It's common to have data that you need to show as a list. You can use array methods to manipulate your data and generate UI elements that are identical in style but hold different pieces of information.
`const names = ['Ada Lovelace', 'Grace Hopper', 'Margaret Hamilton'];`

You can then use the array.map() method to iterate over the array and use an arrow function to map a name to a list item:

If you run this code, React will give us a warning about a missing key prop. This is because React needs something to uniquely identify items in an array so it knows which elements to update in the DOM.

You can use the names for now since they are currently unique, but it's recommended to use something guaranteed to be unique, like an item ID: `<li key={name}>{name}</li>`

## Events
Event names are camelCased, e.g. onClick
You can define a function to "handle" events whenever they are triggered. Create a function before the return statement called handleClick():

## State and Hooks
React has a set of functions called hooks. Hooks allow you to add additional logic such as state to your components. You can think of state as any information in your UI that changes over time, usually triggered by user interaction.
You can use state to store and increment the number of times a user has clicked the "Like" button. In fact, the React hook used to manage state is called: useState()

Add useState() to your project. It returns an array, and you can access and use those array values inside your component using array destructuring:
- The first item in the array is the state value, which you can name anything. It's recommended to name it something descriptive:
- The second item in the array is a function to update the value. You can name the update function anything, but it's common to prefix it with set followed by the name of the state variable you're updating:
- You can also take the opportunity to add the initial value of your likes state to 0:
- `const [likes, setLikes] = React.useState(0);`

**React vs NextJs**\
While React excels at building UI, it does take some work to independently build that UI into a fully functioning scalable application. There are also newer React features, like Server and Client Components, that require a framework. The good news is that Next.js handles much of the setup and configuration and has additional features to help you build React applications.