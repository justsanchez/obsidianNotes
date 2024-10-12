## The Rebirth

tags: #react

Open-sourced in 2013
Initially, a small team at Facebook created React (For their newsfeed feature)

Mentioned followers of using react include:
- Netflix
- Airbnb

React is a javascript framework used for building websites with reusable components

Some useful Features
- Includes JavaScript Syntax Extension (`JSX`)
- Efficient way to update parts of your website
- Fast and Scalable

Initially, before React, *updating a website meant changing the same element in every file*. With react, you change an element once in one place, the change is applied everywhere


**Hot Reloading**: a feature in React that allows developers to instantly see changes made to the code in real-time

#### File Structure
- 📁 **public**
    - 📄 **index.html**: HTML with the root of the React app (i.e., `<div id="root"></div>`).
- 📄 **App.js**: Our React code, written in a cool JavaScript syntax called JSX.
- 📄 **index.js**: The place where our React app is started from.
- 📜 **package.json**: A list of Node packages that help this app run, including React.
- 📄 **styles.css**: Base styles for the React app
#### The Root

The **index.html** file only really holds one element with the id of `"root"`, this is where the React app is run
```HTML
<div id="root"></div>
```

This element is then selected inside the **index.js** file to render the website:

```js
const container = document.getElementById("root")
```
##### Why is it important? 

Because it connects the HTML to the React code

### Code Example

On public/index.html
```HTML
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
	<!-- the root is placed here inside a div -->
    <div id="root"></div>
  </body>
</html>

```

On index.js
```js
import React from "react";
import { createRoot } from "react-dom/client";
import "./styles.css";
import App from "./App";

const container = document.getElementById("root"); 

const root = createRoot(container); 

root.render(<App />);

```


When we import `React` from the `"react"` library, we can use JavaScript Syntax Extension (or "JSX").

When we import React from the "react" library, we can use Javascript Syntax Extension 

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