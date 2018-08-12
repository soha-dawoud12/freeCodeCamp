# Make Typography Responsive

Instead of using `em` or `px` to size text, you can use viewport units for responsive typography. Viewport units, like percentages, are relative units, but they are based off different items. Viewport units are relative to the viewport dimensions (width or height) of a device, and percentages are relative to the size of the parent container element.

The four different viewport units are:

- `vw: 10vw` would be 10% of the viewport's width.

- `vh: 3vh` would be 3% of the viewport's height.

- `vmin: 70vmin` would be 70% of the viewport's smaller dimension (height vs. width).

- `vmax: 100vmax` would be 100% of the viewport's bigger dimension (height vs. width).

---

## Challenge

Set the `width` of the `h2` tag to 80% of the viewport's width and the `width` of the paragraph as 75% of the viewport's smaller dimension.

---

## Tips

- Your `h2` tag should have a `width` of 80vw.

- Your `p` tag should have a `width` of 75vmin.

---

## Solution

```html
<style>
  h2 {
    width:80vw;
  }
  p {
    width:75vmin;
  }
</style>

<h2>Importantus Ipsum</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```