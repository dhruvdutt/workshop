## GitHub Workshop Notes - Changa

### Commands Cheatsheet

1. `git init`: Initialize / create a new local repository. (Do this only once)
2. `git remote add origin [url without brackets]`: Connect your local repo to an online repo. (Do this only once)
3. `git add .`: Add all files to staging area.
4. `git commit -m "first commit"`: Save the changes with a message.
5. `git push origin master`: Upload changes to the master branch of your remote repository.
6. `git pull origin master`: Download and merge changes from the remote repo to your working repo.	

#### Optional Commands

1. `git status`: List the files you've changed and those you still need to add or commit.
2. `git log`: Shows commit history.

#### [More Commands](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)

### Resources

- [Slides](https://docs.google.com/presentation/d/17RmxZUI5mBoBhpttrXj_jiZg5GVax53aKQa7C0AEKXc/edit?usp=sharing)
- [Getting-Started - YouTube](https://www.youtube.com/watch?v=0fKg7e37bQE)
- [Interactive GitHub Tutorial](https://try.github.io/)
- [Udacity Course - 3 weeks certification](https://in.udacity.com/course/how-to-use-git-and-github--ud775)

---

## JavaScript Workshop Notes

### JavaScript Courses

- [LearnCode Academy](https://www.youtube.com/playlist?list=PLoYCgNOIyGACnrXwo5HMCfOH9VT05znGv) *Highly Recommended
- [The New Boston](https://www.youtube.com/playlist?list=PL46F0A159EC02DF82)

- [Mozilla JS docs](https://developer.mozilla.org/bm/docs/Web/JavaScript)
- [W3C JS docs](https://www.w3schools.com/jS/default.asp)

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
