
Links: [[001 React]]
Tags: #react 
Date: 10/13/24

**Components** are pieces of `JSX` that make up most of the website. Think of them as widgets from Flutter. They can be anything from labels to buttons to navigation menus

Example of a component defined with a `function` keyword

```js
import React from "react";

export default function FunctionComponent(){
	return (
	<div> 
		{/* this is a comment */}
		<h1>Heres some markup!</h1>
	</div>
	)
}
```
###### Things to consider
- The name of the component must be in "PascalCase", the name must begin with a capital letter
- The `JSX` returned by a component is bundled under a single element and rendered as a single part, or component, of a website

## Using Components

####  How do we use components after defining them?

We can set them up to be used in other components with the following **`export default`**
```js
export default function FunctionComponent(){


}
```

Then, import the component for use in another component file
```js
import FunctionComponent from "file/path/to/FunctionComponent.js"

function App() {
  return (
    <FunctionComponent />
  )
}
```


Every React Application must be rendered from a  root component. Usually dont like this
```js
import React from "react";
import { createRoot } from "react-dom/client";

export default function App() {
  return (
    <div>
      {/* Returned JSX here */}
    </div>
  )
}

const container = document.getElementById("root");

const root = createRoot(container);

root.render(<App />);
```

We first import the `createRoot()` at the top of the .js file. Then, we define our component (usually named `<App>` or `<Home>`)


