# HTML Lists

HTML lists allow web developers to group a set of related items in lists.

## Unordered HTML List

An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag.

The list items will be marked with bullets (small black circles) by default:

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

## Unordered HTML List - Choose List Item Marker

The CSS `list-style-type` property is used to define the style of the list item marker. It can have one of the following values:

## Unordered HTML List - Choose List Item Marker

The CSS `list-style-type` property is used to define the style of the list item marker. It can have one of the following values:

| Value  | Description                                     |
| :----- | :---------------------------------------------- |
| disc   | Sets the list item marker to a bullet (default) |
| circle | Sets the list item marker to a circle           |
| square | Sets the list item marker to a square           |
| none   | The list items will not be marked               |

```html
<ul style="list-style-type:circle;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

<ul style="list-style-type:circle;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>





## Nested HTML Lists

Lists can be nested (list inside list):

```html
<ul>
  <li>Coffee</li>
  <li>Tea
    <ul>
      <li>Black tea</li>
      <li>Green tea</li>
    </ul>
  </li>
  <li>Milk</li>
</ul>
```

<ul>  <li>Coffee</li>  <li>Tea    <ul>      <li>Black tea</li>      <li>Green tea</li>    </ul>  </li>  <li>Milk</li></ul>

**Note:** A list item (`<li>`) can contain a new list, and other HTML elements, like images and links, etc.





## Horizontal List with CSS

HTML lists can be styled in many different ways with CSS.

One popular way is to style a list horizontally, to create a navigation menu:

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111111;
}
</style>
</head>
<body>

<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>

</body>
</html>
```

<!DOCTYPE html><html><head><style>ul {  list-style-type: none;  margin: 0;  padding: 0;  overflow: hidden;  background-color: #333333;}li {  float: left;}li a {  display: block;  color: white;  text-align: center;  padding: 16px;  text-decoration: none;}li a:hover {  background-color: #111111;}</style></head><body><ul>  <li><a href="#home">Home</a></li>  <li><a href="#news">News</a></li>  <li><a href="#contact">Contact</a></li>  <li><a href="#about">About</a></li></ul></body></html>