# HTML Ordered Lists

The HTML `<ol>` tag defines an ordered list. An ordered list can be numerical or alphabetical.

------

## Ordered HTML List

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.

The list items will be marked with numbers by default:

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol>
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>



## Ordered HTML List - The Type Attribute

The `type` attribute of the `<ol>` tag, defines the type of the list item marker:

| Type     | Description                                                  |
| :------- | :----------------------------------------------------------- |
| type="1" | The list items will be numbered with numbers (default)       |
| type="A" | The list items will be numbered with uppercase letters       |
| type="a" | The list items will be numbered with lowercase letters       |
| type="I" | The list items will be numbered with uppercase roman numbers |
| type="i" | The list items will be numbered with lowercase roman numbers |

```html
<ol type="A">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol type="A">
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>

```html
<ol type="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol type="a">
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>

```html
<ol type="I">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol type="I">
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>

```html
<ol type="i">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol type="i">
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>



## Control List Counting

By default, an ordered list will start counting from 1. If you want to start counting from a specified number, you can use the `start` attribute:

```html
<ol start="50">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<ol start="50">
 <li>Coffee</li>
 <li>Tea</li>
 <li>Milk</li>
</ol>





## Nested HTML Lists

Lists can be nested (list inside list):

```html
<ol>
  <li>Coffee</li>
  <li>Tea
    <ol>
      <li>Black tea</li>
      <li>Green tea</li>
    </ol>
  </li>
  <li>Milk</li>
</ol>
```

<ol>  <li>Coffee</li>  <li>Tea    <ol>      <li>Black tea</li>      <li>Green tea</li>    </ol>  </li>  <li>Milk</li></ol>

**Note:** A list item (`<li>`) can contain a new list, and other HTML elements, like images and links, etc.