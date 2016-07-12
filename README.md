# candy.scss

A Sass utility to produce duplicate CSS with many different colors. Let's say you've got six elements, and you want each one to have a different set of colors. You might write CSS like this:

```css
.box:nth-child(1) { color: red; }
.box:nth-child(1) { color: #a06000; }
.box:nth-child(1) { color: #c04000; }
.box:nth-child(1) { color: #df2000; }
.box:nth-child(1) { color: purple; }
```

candy.css streamlines this down to one chunk of CSS. You tell the mixin what the start and end colors of the gradient, and how many elements you need.

```scss
.box {
  @include candy(red, purple) {
    color: candy-color();
  }
}
```
