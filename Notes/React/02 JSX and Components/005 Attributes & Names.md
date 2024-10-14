
Links: [[001 React]]
Tags: #react 
Date: 10/12/24


Just like in HTML, `JSX` supports attributes. Any valid HTML and their associated attributes are supported in JSX...mostly

For example, `src` and `alt`
```js
const selfie = <img src="username/camera/recents/today.png" alt="a selfie" />
```

The widely used attribute in HTML is `class`
```HTML
<button class="login-button">
  Submit
</button>
```

However the `JSX` equivalent to `class` is **`className`**

In JavaScript, `class` is a reserved keyword. Therefore, we use `className`

Sample Code
```js
export default function App() {
  const barcelonaImage = <img src= "https://i.imgur.com/qaQNzqi.png"  alt="Barcelona" />;
  const tokyoImage = <img src="https://i.imgur.com/OAx1wzO.png"  alt="Tokyo" />;
  const ohioImage = <img src="https://i.imgur.com/CxJjltu.png"  alt="Ohio" />;

  const imageGallery = [
    <li>{barcelonaImage}</li>,
    <li>{tokyoImage}</li>,
    <li>{ohioImage}</li>
  ]

  return (
    <ul>
      {imageGallery}
    </ul>
  );
}
```