# HTML Iframes

An HTML iframe is used to display a web page within a web page.

------

## HTML Iframe Syntax

The HTML `<iframe>` tag specifies an inline frame.

An inline frame is used to embed another document within the current HTML document.

- Syntax

  ```html
  <iframe src="url" title="description">
  ```

- **Tip:** It is a good practice to always include a `title` attribute for the `<iframe>`. This is used by screen readers to read out what the content of the iframe is.





## Iframe - Set Height and Width

Use the `height` and `width` attributes to specify the size of the iframe.

The height and width are specified in pixels by default:

```html
<iframe src="demo_iframe.htm" height="200" width="300" title="Iframe Example"></iframe>
```

![image-20201219130014946](https://i.loli.net/2020/12/19/bP7d3ESVuhGJYBU.png)





## Iframe - Remove the Border

By default, an iframe has a border around it.

To remove the border, add the `style` attribute and use the CSS `border` property:

```html
<iframe src="demo_iframe.htm" style="border:none;" title="Iframe Example"></iframe>
```

With CSS, you can also change the size, style and color of the iframe's border:

```html
<iframe src="demo_iframe.htm" style="border:2px solid red;" title="Iframe Example"></iframe>
```





## Iframe - Target for a Link 

An iframe can be used as the target frame for a link.

The `target` attribute of the link must refer to the `name` attribute of the iframe:

```html
<iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p> #在iframe_a这个target frame中显示w3school网站
```

