# Fluid, fixed width and Responsive Pages

## Fluid early days

In the early days of web pages, structure types tended to be fluid, meaning a web page stretched and resized as the browser did to always fill the viewport. This is where the “fluid” name comes from: It fills every area of the web page regardless of its size, just like a fluid fills its container.

A web page, by default, is fluid. The reason is that the initial value for an element’s width is auto, which tells the browser to work out the width itself, based on the unused space around that element. Without any CSS applied to a page—other than the user agent stylesheet— width: auto is the equivalent of width: 100%.


Fluid-width websites are often used when a page has a lot of information and the designer wants to make the most of the space available.

## Fixed Width for more control

If a fluid page stretched depending on the browser win- dow size, designers would have a difficult job designing a web page because they couldn’t be sure how that page would look to the users. The majority of the web started making use of the fixed-width layout

Fixed-width layouts are made by giving the element that contains the rest of the page’s elements a width property. The width property is usually a pixel value such as 960px, which makes the <body> element always 960px, regardless of the size of the browser.

#### Why a width of 960px?

When the web was accessed by fewer types of devices (mainly the only consideration was differing desktop display sizes), it was wise to use a width of 960px because the most-used screen resolution was 1,024 × 768, meaning that 960px would fit nicely into a 1,024px display (as shown in Figure 6-1), as well as anything bigger than that. If a web page is 1,260px wide and is viewed on a screen 1,024px wide, the browser has to show horizontal scroll bars to allow the user to move across to see the full

## Responsive design

With new technologies such as CSS3 and HTML5, and in particular the CSS3 media queries, the web is moving toward responsive layouts that start with a fluid structure but then change that layout based on the size of a device—something that couldn’t be done when fluid layouts were first in use.

## Fluid Images

It is very common to see the images broken. ie. they will be using their original width. which could be more than their container or sometimes way less than they should be.
To fix this we can add this style
```css
img {
  max-width: 100%;
}
```

## Adaptive Design
Where a responsive design uses a fluid layout and media queries to make a web page change its layout for every different width, an adaptive design uses a fixed layout and media queries to change the layout only when specific width conditions are met. A responsive design changes its layout for every different pixel width, whereas an adaptive design may change its layout several times: one for mobile, one for tablets, and one for desktop/laptops, for example.


## Mobile first design

This mobile first mindset forces you to think about what is the most important content to display in the space available. You can then slowly build up the less relevant content as and when you have more space to play with. This approach has performance benefits too—for mobile devices that typically have less processing power and generally less bandwidth than other devices.
