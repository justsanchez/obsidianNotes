
Links: [[001 React]]
Tags: #react 
Date: 10/12/24

#### What are apps made of 

Components - defined like functions that **return** `JSX` content

- `JSX` - is like the language of react
- Components - are like the building blocks of react of the user UI

Short Sample Example, functional component that returns some `JSX`
```js
import React from "react";

export default function App(){
	return(
		<div>
			<h1>Hello World!</h1>
			<p>Nice to meet you</p>
		</div>
	)
}
```

**Note:** The returned `JSX` must be wrapped in a single element, meaning for example 2 div elements or more can't be returned. It'll try an error

*`export default`*: lets us use the component in other files
