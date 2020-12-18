# HTML Block and Inline Elements

Every HTML element has a default display value, depending on what type of element it is.

There are two display values: block and inline.

------

## Block-level Elements

A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

The `<div>` element is a block-level element.

```html
<div>Hello World</div>
```

<div>Hello World</div>

![image-20201218221826733](https://i.loli.net/2020/12/19/bRCKg41QUpy5vXl.png)





## Inline Elements

An inline element does not start on a new line and it only takes up as much width as necessary.

This is a `<span>` element inside a paragraph.

```html
<span>Hello World</span>
```

<span>Hello World</span>

![image-20201218221913795](https://i.loli.net/2020/12/19/cxNnAGpJsBqjeTS.png)

- **Note:** An inline element cannot contain a block-level element!





## The `<div>` Element

- The `<div>` element is often used as a container for other HTML elements.

- The `<div>` element has no required attributes, but `style`, `class` and `id` are common.

- When used together with CSS, the `<div>` element can be used to style blocks of content:

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div>
```

<div style="background-color:black;color:white;padding:20px;">  <h2>London</h2>  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p></div>





## The `<span>` Element

- The `<span>` element is an inline container used to mark up a part of a text, or a part of a document.

- The `<span>` element has no required attributes, but `style`, `class` and `id` are common.

- When used together with CSS, the `<span>` element can be used to style parts of the text:

```html
<p>My mother has <span style="color:blue;font-weight:bold">blue</span> eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes.</p>
```

<p>My mother has <span style="color:blue;font-weight:bold">blue</span> eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes.</p>