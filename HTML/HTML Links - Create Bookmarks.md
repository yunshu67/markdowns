# HTML Links - Create Bookmarks

HTML links can be used to create bookmarks, <u>so that readers can jump to specific parts of a web page.</u>





## Create a Bookmark in HTML

- Bookmarks can be useful if a web page is very long.

- To create a bookmark - first create the bookmark, then add a link to it.

- When the link is clicked, the page will scroll down or up to the location with the bookmark.

- e.g.

  First, use the `id` attribute to create a bookmark

  Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:

```html
<h2 id="C4">Chapter 4</h2> 								# 创造一个heading， 且这个heading有一个bookmark
<a href="#C4">Jump to Chapter 4</a>						# 该链接跳转到C4书签 
```

<h2 id="C4">Chapter 4</h2>
<a href="html_demo.html#C4">Jump to Chapter 4</a>



- e.g.

  You can also add a link to a bookmark on another page:


```html
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```