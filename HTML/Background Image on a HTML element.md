## Background Image on a HTML element

To add a background image on an HTML element, use the HTML `style` attribute and the CSS `background-image` property

- A background image can be specified for almost any HTML element.

```html
<div style="background-image: url('img_girl.jpg');">
```





## Background Image on a Page

If you want the entire page to have a background image, you must specify the background image on the `<body>` element:

```html
<style>
body {
  background-image: url('img_girl.jpg');
}
</style>
```





## Background Repeat

If the background image is smaller than the element, the image will repeat itself, horizontally and vertically, until it reaches the end of the element:

![image-20201217221417463](https://i.loli.net/2020/12/18/jYWnuRTOfLcG6pC.png)

To avoid the background image from repeating itself, set the `background-repeat` property to `no-repeat`.

```html
<style>
body {
  background-image: url('example_img_girl.jpg');
  background-repeat: no-repeat;
}
</style>
```





## Background Cover

If you want the background image to cover the entire element, you can set the `background-size` property to `cover.`

Also, to make sure the entire element is always covered, set the `background-attachment` property to `fixed:`

This way, the background image will cover the entire element, with no stretching (the image will keep its original proportions):

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
```

## Background Stretch

If you want the background image to stretch to fit the entire element, you can set the `background-size` property to `100% 100%`:

![image-20201217221651335](https://i.loli.net/2020/12/18/yl5gDc4YXrM1mLp.png)

Try resizing the browser window, and you will see that the image will stretch, but always cover the entire element.

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
</style>
```

