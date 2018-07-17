## JavaScript Workshop Notes

### JavaScript Basics

- [Exercise](https://codesandbox.io/s/8kk1m79838)

---

## DOM - Document Object Model

### Basics - `window`

#### `window.location` - Redirect

```js
window.location.href = "https://github.com/dhruvdutt";
```

#### `window.location` - New Tab

```js
window.open("https://github.com/dhruvdutt");
```

---


### Basics - `document` selectors

#### `getElementById`: get by ID

```js
document.getElementById("element-id"); // returns matched element
```

#### `getElementsByClassName`: get by ID

```js
document.getElementsByClassName("element-class"); // returns array of matched elements
```

#### `createElement`: create new element

```js
document.createElement("p");
```

### Examples:

#### Add element in body

```js
 // create a couple of elements in an otherwise empty HTML page
let heading = document.createElement("h1");
let heading_text = document.createTextNode("Big Head!");
heading.appendChild(heading_text);
document.body.appendChild(heading);
```

#### [`onclick`](https://codesandbox.io/s/6ll1zwmy63) attribute

#### `click` listener

```js
element.addEventListener("click", function() {
    console.log("Listener func called");
});
```

### `keyDown` listener

#### [key codes](http://keycode.info/)

```html
<input type="text" id="inp" size="50" onkeydown="keyCode(event)"></input> 

<script>
function keyCode(event) {
    var x = event.keyCode;
    if (x == 27) {
      document.getElementById("inp").value = "";
    }
}
</script>
```

#### [CSS border example](https://codesandbox.io/s/2vjpyynpnn)


#### Timeout: run ***after*** x seconds

```js
setTimeout(function() {
  console.log("Will log after 3 seconds");
}, 3000);
```

#### Interval: run ***every*** x seconds

```js
setInterval(function() {
  console.log("Will log every 3 seconds");
}, 3000);
```

#### `onkeydown`

```html
<p>Enter mobile number:</p>
<input type="number" onkeydown="checkNumber(this.value)">

<script>
function checkNumber(number) {
    console.log(number);
}
</script>
```

#### API call `fetch`

```html
<script>
let URL = "https://cors.io/?http://www.mocky.io/v2/5a7f23442e00005000b56873";

fetch(URL)
  .then(response => response.json())
  .then(response => {
    console.log(response);
  })
  .catch(error => {
    console.log(error);
  })
</script>
```
