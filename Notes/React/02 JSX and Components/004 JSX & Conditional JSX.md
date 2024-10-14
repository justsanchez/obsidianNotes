
Links: [[001 React]]
Tags: #react 
Date: 10/12/24


## A new way of Javascript

![[Pasted image 20241012203614.png]]

This is **JSX**
```js
let header = <header>Compiler Coffee ☕</header>;
```


Parts of **JSX** are disguised as HTML, when the react app is ran; the HTML-like parts are transpiled into browser-readable JavaScript!

More **JSX**
```js
function addHeading() {
  return (
    <div>
      <header>Compiler Coffee ☕</header>
      <p>Our coffee is home brewed!</p>
    </div>
  )
}
```
Or
```js
export default function App() {
  // adding js to JSX
  let headerElement = <header>Compiler Coffee ☕</header>;
  const paragraph = Our coffee is home brewed!;
  // multi-line wrap in parentheses to make it more readable!
  return (
	  <div> 
		  {headerElement} 
		  <p>{paragraph}</p>
	  </div>
	  )
}

```

**Always remember, you can only return a single element**


## Conditional JSX

JSX can be **rendered conditionally**, we can use the conditional statements to determine exactly what JSX should be displayed

```js
let page = null;
let signedIn= true;

if (signedIn) {
	page = <div>User dashboard</div>
} else {
	page = <div>Sign-in Page</div>
}

export default function App(){
	return (
	<div>
		{page}
	</div>
	)
}
```

#### Ternary Operators

Traditional Conditional
```js
if (condition) { 
	// Run if true 
}  else { 
	// Run if false 
}
```

**Ternary operators**- are used as a shorthand for an `if/else` statement
```js
condition ? ifTrue : ifFalse;
```

Use cases:
- Raw data (Numbers, Strings, etc.)
- Defined variable with a value
- A function that returns a value, like `console.log()`

Traditional example
```js
let num = Math.random();

if (num > 0.5) {
  console.log("Heads");
} else {
  console.log("Tails");
}
```

Using Ternary operators
```js
let num = Math.random();

let coinFlip = num > .5 ? "Heads" : "Tails"
console.log(coinFlip);
```

##### If no else condition is present 
We can use `&&` ("and") or `||` ("or")

Using `&&`
```js
let element = {condition && <div>Content to display when condition is true</div>}

// use cases
{condition && <div>Condition is true</div>}
{!condition && <div>Condition is false</div>}
```
*In this example, `<div>`will only be rendered if the condition is true*

Using `||`
If the condition is falsy (e.g., false, null, undefined, 0, or an empty string), it will render the fallback component.
```js
let element = {condition || <div>Fallback content to display when condition is false</div>}
```
*In this example, if the condition is falsy, `<div>` will be rendered. Otherwise, it will display the value of the condition itself if it’s truthy.*
