# Improving the Perceived Performance of Page

## Improving perception of load time of image by setting average color of image as background
Some sites have very large images that, even when optimized, took a little while to load. A bunch of stuff can be done in order to prefetch the image, fire off its request earlier, etc., but one of the simplest techniques to employ is to apply the image’s average color as a background-color, so that the user isn't looking at a huge white space whilst the image loaded. This improves perceived performance dramatically, and is an incredibly low-effort implementation

```css
.background-image {
  background-image: url(/img/bg.jpg);
  background-color: #3d3e5b;
}
```
