# HTML - The Head Element

The HTML `<head>` element is a container for the following elements: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, and `<base>`.

------

## The HTML `<head>` Element

The `<head>` element is a container for ***metadata*** (data about data) and is placed between the `<html>` tag and the `<body>` tag.

HTML metadata is data about the HTML document. <u>Metadata is not displayed.</u>

Metadata typically define the document title, character set, styles, scripts, and other meta information.





## The HTML `<title>` Element

- The `<title>` element defines the title of the document. The title must be text-only, and <u>it is shown in the browser's title bar or in the page's tab.</u>

- The `<title>` element is required in HTML documents!

- The contents of a page title is very important for search engine optimization (SEO)! The page title is used by search engine algorithms to decide the order when listing pages in search results.

The `<title>` element:

- defines a title in the browser toolbar
- provides a title for the page when it is added to favorites
- displays a title for the page in search engine-results

So, try to make the title as accurate and meaningful as possible!

A simple HTML document:

```html
<!DOCTYPE html>
<html>
<head>
  <title>A Meaningful Page Title</title>
</head>
<body>

<p>The content of the body element is displayed in the browser window.</p>
<p>The content of the title element is displayed in the browser tab, in favorites and in search-engine results.</p>

</body>
</html>
```

[demo](http://htmlpreview.github.io/?https://github.com/yunshu67/personal-projects/blob/main/mini-projects/HTML/title.html)





## The HTML `<style>` Element

The `<style>` element is used to define style information for a single HTML page:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
  <style>
    body {background-color: powderblue;}
    h1 {color: red;}
    p {color: blue;}
  </style>
</head>  
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>
  
</body>
</html>
```





## The HTML `<link>` Element

The `<link>` element defines the relationship between the current document and an external resource.

The `<link>` tag is most often used to link to external style sheets:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
  <link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>
  
</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_link)





## The HTML `<meta>` Element

The `<meta>` element is typically used to specify the character set, page description, keywords, author of the document, and viewport settings.

The metadata will not be displayed on the page, but are used by browsers (how to display content or reload page), by search engines (keywords), and other web services.

![image-20201219200212042](https://i.loli.net/2020/12/20/EzHNOQAV5duPo9M.png)

Example of `<meta>` tags:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Free Web tutorials">
  <meta name="keywords" content="HTML, CSS, JavaScript">
  <meta name="author" content="John Doe">
</head>
<body>

<p>All meta information goes inside the head section.</p>

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_meta)





## Setting The Viewport

The viewport is the user's visible area of a web page. It varies with the device - it will be smaller on a mobile phone than on a computer screen.

You should include the following `<meta>` element in all your web pages:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This gives the browser instructions on how to control the page's dimensions and scaling.

- The `width=device-width` part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).

- The `initial-scale=1.0` part sets the initial zoom level when the page is first loaded by the browser.

Here is an example of a web page *without* the viewport meta tag, and the same web page *with* the viewport meta tag:





**Tip:** If you are browsing this page with a phone or a tablet, you can click on the two links below to see the difference.



[![img](https://www.w3schools.com/css/img_viewport1.png)

**Without the viewport meta tag**](https://www.w3schools.com/html/example_withoutviewport.htm)



[![img](https://www.w3schools.com/css/img_viewport2.png)

**With the viewport meta tag**](https://www.w3schools.com/html/example_withviewport.htm)





## The HTML `<script>` Element

The `<script>` element is used to define client-side JavaScripts.

The following JavaScript writes "Hello JavaScript!" into an HTML element with id="demo":





## The HTML `<base>` Element

- **The `<base>` element specifies the base URL and/or target for all relative URLs in a page.**

- The `<base>` tag must have either an href or a target attribute present, or both.

- There can only be one single `<base>` element in a document!

```html
<!DOCTYPE html>
<html>
<head>
  <base href="https://www.w3schools.com/" target="_blank">
</head>
<body>

<h1>The base element</h1>

<p><img src="images/stickman.gif" width="24" height="39" alt="Stickman"> - Notice that we have only specified a relative address for the image. Since we have specified a base URL in the head section, the browser will look for the image at "https://www.w3schools.com/images/stickman.gif".</p>

<p><a href="tags/tag_base.asp">HTML base tag</a> - Notice that the link opens in a new window, even if it has no target="_blank" attribute. This is because the target attribute of the base element is set to "_blank".</p>

</body>
</html>
```

[demo](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_base)