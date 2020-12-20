# HTML JavaScript

JavaScript makes HTML pages more dynamic and interactive.

------

```html
<!DOCTYPE html>
<html>
<body>

<h1>My First JavaScript</h1>

<button type="button"
onclick="document.getElementById('demo').innerHTML = Date()">
Click me to display Date and Time.</button>

<p id="demo"></p>

</body>
</html> 
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_scripts_intro)





## The HTML `<script>` Tag

- The HTML `<script>` tag is used to define a client-side script (JavaScript).

- The `<script>` element either contains script statements, or it points to an external script file through the `src` attribute.

- Common uses for JavaScript are image manipulation, form validation, and dynamic changes of content.

- To select an HTML element, JavaScript most often uses the `document.getElementById()` method.

This JavaScript example writes "Hello JavaScript!" into an HTML element with id="demo":

```html
<!DOCTYPE html>
<html>
<body>

<h2>Use JavaScript to Change Text</h2>
<p>This example writes "Hello JavaScript!" into an HTML element with id="demo":</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script> 

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script)





## A Taste of JavaScript

Here are some examples of what JavaScript can do:

1. JavaScript can change content:

```html
<!DOCTYPE html>
<html>
<body>

<h1>My First JavaScript</h1>

<p>JavaScript can change the content of an HTML element:</p>

<button type="button" onclick="myFunction()">Click Me!</button>

<p id="demo">This is a demonstration.</p>

<script>
function myFunction() { 
  document.getElementById("demo").innerHTML = "Hello JavaScript!";
}
</script>

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script_html)

2. JavaScript can change styles:

```html
<!DOCTYPE html>
<html>
<body>

<h1>My First JavaScript</h1>

<p id="demo">JavaScript can change the style of an HTML element.</p>

<script>
function myFunction() {
  document.getElementById("demo").style.fontSize = "25px"; 
  document.getElementById("demo").style.color = "red";
  document.getElementById("demo").style.backgroundColor = "yellow";        
}
</script>

<button type="button" onclick="myFunction()">Click Me!</button>

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script_styles)

3. JavaScript can change attributes:

```html
<!DOCTYPE html>
<html>
<body>

<h1>My First JavaScript</h1>
<p>Here, a JavaScript changes the value of the src (source) attribute of an image.</p>

<script>
function light(sw) {
  var pic;
  if (sw == 0) {
    pic = "pic_bulboff.gif"
  } else {
    pic = "pic_bulbon.gif"
  }
  document.getElementById('myImage').src = pic;
}
</script>

<img id="myImage" src="pic_bulboff.gif" width="100" height="180">

<p>
<button type="button" onclick="light(1)">Light On</button>
<button type="button" onclick="light(0)">Light Off</button>
</p>

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script_attribute)





## The HTML `<noscript>` Tag

The HTML `<noscript>` tag defines an alternate content to be displayed to users that have disabled scripts in their browser or have a browser that doesn't support scripts:

```html
<!DOCTYPE html>
<html>
<body>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>

<noscript>Sorry, your browser does not support JavaScript!</noscript>

<p>A browser without support for JavaScript will show the text written inside the noscript element.</p>
 
</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_noscript)