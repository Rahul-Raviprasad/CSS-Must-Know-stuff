# Improving the Perceived Performance of Page

Anything less than one second is perceived as ‘instant’ behaviour, it is almost unnoticeable. Up to one second is immediate, anything more than this is when the user realises they are waiting.

## Preloading some of the content
like you can preload some of the user information earlier and display loading for an image which say takes more time. Not freezing the entire screen for the user. So the user is actively looking at some information or interacting with the page.

## Justifying to customers

Your page needs to load 20% faster for your users to notice any difference. If your page takes 8s to load today, a new version needs to take 6.4s to load for it to feel faster. Anything less than 20% is difficult to justify.

## Improving perception of load time of image by setting average color of image as background
Some sites have very large images that, even when optimized, took a little while to load. A bunch of stuff can be done in order to prefetch the image, fire off its request earlier, etc., but one of the simplest techniques to employ is to apply the image’s average color as a background-color, so that the user isn't looking at a huge white space whilst the image loaded. This improves perceived performance dramatically, and is an incredibly low-effort implementation

```css
.background-image {
  background-image: url(/img/bg.jpg);
  background-color: #3d3e5b;
}
```

Here’s a short step-by-step guide to ensuring you are considering performance when designing:

* Research the priority content that should load in your interface. If it’s a news article, the text content should load first, allowing the user to start reading before the experience has even finished loading.
* Provide a loading state (e.g. placeholder content) and a fallback (e.g. un-styled text) for all elements you design and use.
* Work with the developers to fine tune performance and work out what technologies can be used to ensure quick loading (e.g. browser caching and progressive jpegs).

## progress bars > loading
whenever possible to show the estimate on how much is pending, use a progress bar. as it lets the user know what to expect.

## use animations to give smooth flow and mask the loading time


Sources
http://www.chrisharrison.net/projects
http://www.chrisharrison.net/projects/progressbars2/ProgressBarsHarrison.pdf
