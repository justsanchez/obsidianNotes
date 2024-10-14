
Links: [[001 React]]
Tags: #react 
Date: 10/13/24

## One way data

In React, "*attributes*" (e.g., `className="example"`) are more commonly known as *props*

**Props** are pieces of data that are given to `JSX` elements for them to use or pass from parent to child component. You can use any data type for props, including objects and functions!

```js
function App () {
  return <img src="selfie.png" alt="my selfie" />
}
```
###### In the example above, we passed the data to the `src` and `alt` props of the `<img>` element

Passing down a array of objects
```js
export default function App() {
  const catalogItems = [
{
  name: "Dan",
  category: "Developer",
  website: "dandeveloper.dev"
}, 
{
  name: "Alvaro",
  category: "Mexican",
  website: "landscaping.dev"
}
						]
  return (
  <div>
    {catalogItems.map(function (item)
      {
        return (
          <div>
            <h2>{item.name}</h2>
            <h3>{item.category}</h3>
            {/*  The `<a>`anchor element is using a `href` prop */}
            <a href={item.website}>Learn more</a>
          </div>
        )
      }                         
    )}
  </div>
  );
}

```
