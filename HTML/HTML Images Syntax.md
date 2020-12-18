## HTML Images Syntax

The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

<u>The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.</u>

The `<img>` tag has two required attributes:

- src - Specifies the path to the image
- alt - Specifies an alternate text for the image

```html
<img src="url" alt="alternatetext">
```





## The src Attribute

The required `src` attribute specifies the path (URL) to the image.

**Note:** When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon and the `alt` text are shown if the browser cannot find the image.





## The alt Attribute

The required `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).

The value of the `alt` attribute should describe the image:





## Image Size - Width and Height

You can use the `style` attribute to specify the width and height of an image.

```html
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">
```

Alternatively, you can use the `width` and `height` attributes:

```html
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```

The `width` and `height` attributes always define the width and height of the image in pixels.





## Width and Height, or Style?

The `width`, `height`, and `style` attributes are all valid in HTML.

<u>However, we suggest using the `style` attribute</u>. It prevents styles sheets from changing the size of images.





## Image as a Link

To use an image as a link, put the `<img>` tag inside the `<a>` tag:

```html
<a href="default.asp">
  <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
```







## Image Floating

Use the CSS `float` property to let the image float to the right or to the left of a text:

```html
<p><img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
The image will float to the right of the text.</p>

<p><img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
The image will float to the left of the text.</p>

```

![image-20201217215811365](https://i.loli.net/2020/12/18/wtiomY2U318Kfsg.png)