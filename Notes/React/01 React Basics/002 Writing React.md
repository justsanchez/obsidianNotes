
Links: [[001 React]]
Tags: #react 
Date: 10/12/24

## React Syntax 

When we import React from the `"react"` library, we can use Javascript Syntax Extension `JSX`

Notice the syntax looks like HTML inside Javascript
**Sample** **`JSX`**
```js
// Before being transpiled
let heading = <h1 id="welcome-heading">Welcome!</h1>
// After being transpiled
let heading = React.createElement("h1", { id: "welcome-heading" }, "Welcome!");
```


In app.js

```JS
export default function App(){
return (
	<div>
		<h1> Hello World </h1>
	</div>
	)
}
```
