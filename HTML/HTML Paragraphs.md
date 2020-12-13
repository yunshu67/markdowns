## HTML Paragraphs

The HTML `<p>` element defines a paragraph.

A paragraph always starts on a new line, and browsers automatically add some white space (a margin) before and after a paragraph.

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

<p>This is a paragraph.</p><p>This is another paragraph.</p>





## HTML Display

You cannot be sure how HTML will be displayed.

Large or small screens, and resized windows will create different results.

With HTML, you cannot change the display by adding extra spaces or extra lines in your HTML code.

The browser will automatically remove any extra spaces and lines when the page is displayed:





## HTML Horizontal Rules

- The `<hr>` tag defines a **thematic break** in an HTML page, and is most often displayed as a horizontal rule.

- The `<hr>` element is used to separate content (or define a change) in an HTML page:

```html
<h1>This is heading 1</h1>
<p>This is some text.</p>
<hr>
<h2>This is heading 2</h2>
<p>This is some other text.</p>
<hr>
```

<h1>This is heading 1</h1>
<p>This is some text.</p>
<hr>
<h2>This is heading 2</h2>
<p>This is some other text.</p>
<hr>

- The `<hr>` tag is an empty tag, which means that it has no end tag.







## HTML Line Breaks

The HTML `<br>` element defines a line break.

Use `<br>` if you want a line break (a new line) without starting a new paragraph:

```html
<p>This is<br>a paragraph<br>with line breaks.</p>
```

<p>This is<br>a paragraph<br>with line breaks.</p>

- The `<br>` tag is an empty tag, which means that it has no end tag.





## The Poem Problem

This poem will display on a single line:

```html
<p>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</p>
```

<p>  My Bonnie lies over the ocean.  My Bonnie lies over the sea.  My Bonnie lies over the ocean.  Oh, bring back my Bonnie to me.</p>

#### Solution - The HTML <pre> Element

- The HTML `<pre>` element defines preformatted text.

- The text inside a `<pre>` element is displayed in a fixed-width font (usually Courier), and it preserves both spaces and line breaks:

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```

![image-20201213154511572](https://i.loli.net/2020/12/13/rvES2TbG75sn3CF.png)

