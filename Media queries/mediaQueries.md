# Media Queries

It is a module of CSS that defines expressions allowing to tailor presentations to a specific range of output devices without changing the content itself.

## Syntax
media queries consist of media type, contain zero or more expressions.

These expressions resolve to a boolean.
The result of the query is true if  the media type specified in  the media query matches the type of device and the document is being displayed on and all expressions in the media query are true.

```
<!-- CSS media query on a link element -->
<link rel="stylesheet" media="(max-width: 800px)" href="example.css" />

<!-- CSS media query within a stylesheet -->
<style>
@media (max-width: 600px) {
  .facet_sidebar {
    display: none;
  }
}
</style>
```

style sheets in the link tags will still download even if media queries would return(Although they will not apply)

## Logical operators
Complex media queries can be formed using logcal operators like "and", "only" and "not".

### "and"
This requires each chained feature to return true in order for the query to be true.

### "not"
Negates entire media query

### "only"
this is used to apply style only when entire media query matches.

Note: for "not" and "only" operators, you must specify an explicit media type.


## Design decision

There can pitfalls in device specific breakpoints.

1. Always choose breakpoints based on your design and not you device.

Device breakpoints
Sometimes we just have to fix something only on a specific device. Only then we should be using this.

 ```css
/*---------------IPhones-------------------*/

 /* ----------- iPhone 4 and 4S ----------- */

 /* Portrait and Landscape */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 480px)
   and (-webkit-min-device-pixel-ratio: 2) {

 }

 /* Portrait */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 480px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: portrait) {
 }

 /* Landscape */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 480px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: landscape) {

 }

 /* ----------- iPhone 5 and 5S ----------- */

 /* Portrait and Landscape */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 568px)
   and (-webkit-min-device-pixel-ratio: 2) {

 }

 /* Portrait */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 568px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: portrait) {
 }

 /* Landscape */
 @media only screen
   and (min-device-width: 320px)
   and (max-device-width: 568px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: landscape) {

 }

 /* ----------- iPhone 6 ----------- */

 /* Portrait and Landscape */
 @media only screen
   and (min-device-width: 375px)
   and (max-device-width: 667px)
   and (-webkit-min-device-pixel-ratio: 2) {

 }

 /* Portrait */
 @media only screen
   and (min-device-width: 375px)
   and (max-device-width: 667px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: portrait) {

 }

 /* Landscape */
 @media only screen
   and (min-device-width: 375px)
   and (max-device-width: 667px)
   and (-webkit-min-device-pixel-ratio: 2)
   and (orientation: landscape) {

 }

 /* ----------- iPhone 6+ ----------- */

 /* Portrait and Landscape */
 @media only screen
   and (min-device-width: 414px)
   and (max-device-width: 736px)
   and (-webkit-min-device-pixel-ratio: 3) {

 }

 /* Portrait */
 @media only screen
   and (min-device-width: 414px)
   and (max-device-width: 736px)
   and (-webkit-min-device-pixel-ratio: 3)
   and (orientation: portrait) {

 }

 /* Landscape */
 @media only screen
   and (min-device-width: 414px)
   and (max-device-width: 736px)
   and (-webkit-min-device-pixel-ratio: 3)
   and (orientation: landscape) {

 }

 /*   -----   Samsung Galaxy ------- */
 /* Portrait and Landscape */
 @media screen
   and (device-width: 320px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3) {

 }

 /* Portrait */
 @media screen
   and (device-width: 320px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3)
   and (orientation: portrait) {

 }

 /* Landscape */
 @media screen
   and (device-width: 320px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3)
   and (orientation: landscape) {

 }

 /* ----------- Galaxy S5 ----------- */

 /* Portrait and Landscape */
 @media screen
   and (device-width: 360px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3) {

 }

 /* Portrait */
 @media screen
   and (device-width: 360px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3)
   and (orientation: portrait) {

 }

 /* Landscape */
 @media screen
   and (device-width: 360px)
   and (device-height: 640px)
   and (-webkit-device-pixel-ratio: 3)
   and (orientation: landscape) {

 }

 /*------ HTC One ----*/

 /* ----------- HTC One ----------- */

/* Portrait and Landscape */
@media screen
  and (device-width: 360px)
  and (device-height: 640px)
  and (-webkit-device-pixel-ratio: 3) {

}

/* Portrait */
@media screen
  and (device-width: 360px)
  and (device-height: 640px)
  and (-webkit-device-pixel-ratio: 3)
  and (orientation: portrait) {

}

/* Landscape */
@media screen
  and (device-width: 360px)
  and (device-height: 640px)
  and (-webkit-device-pixel-ratio: 3)
  and (orientation: landscape) {

}


/*-----TABS -------------*/

/* ----------- iPad mini ----------- */

/* Portrait and Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* Portrait */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: portrait)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: landscape)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* ----------- iPad 1 and 2 ----------- */
/* Portrait and Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* Portrait */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: portrait)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: landscape)
  and (-webkit-min-device-pixel-ratio: 1) {

}

/* ----------- iPad 3 and 4 ----------- */
/* Portrait and Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (-webkit-min-device-pixel-ratio: 2) {

}

/* Portrait */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: portrait)
  and (-webkit-min-device-pixel-ratio: 2) {

}

/* Landscape */
@media only screen
  and (min-device-width: 768px)
  and (max-device-width: 1024px)
  and (orientation: landscape)
  and (-webkit-min-device-pixel-ratio: 2) {

}

/* ----------- Galaxy Tab 10.1 ----------- */

/* Portrait and Landscape */
@media
  (min-device-width: 800px)
  and (max-device-width: 1280px) {

}

/* Portrait */
@media
  (max-device-width: 800px)
  and (orientation: portrait) {

}

/* Landscape */
@media
  (max-device-width: 1280px)
  and (orientation: landscape) {

}

/* ----------- Asus Nexus 7 ----------- */

/* Portrait and Landscape */
@media screen
  and (device-width: 601px)
  and (device-height: 906px)
  and (-webkit-min-device-pixel-ratio: 1.331)
  and (-webkit-max-device-pixel-ratio: 1.332) {

}

/* Portrait */
@media screen
  and (device-width: 601px)
  and (device-height: 906px)
  and (-webkit-min-device-pixel-ratio: 1.331)
  and (-webkit-max-device-pixel-ratio: 1.332)
  and (orientation: portrait) {

}

/* Landscape */
@media screen
  and (device-width: 601px)
  and (device-height: 906px)
  and (-webkit-min-device-pixel-ratio: 1.331)
  and (-webkit-max-device-pixel-ratio: 1.332)
  and (orientation: landscape) {

}

/* ----------- Kindle Fire HD 7" ----------- */

/* Portrait and Landscape */
@media only screen
  and (min-device-width: 800px)
  and (max-device-width: 1280px)
  and (-webkit-min-device-pixel-ratio: 1.5) {

}

/* Portrait */
@media only screen
  and (min-device-width: 800px)
  and (max-device-width: 1280px)
  and (-webkit-min-device-pixel-ratio: 1.5)
  and (orientation: portrait) {
}

/* Landscape */
@media only screen
  and (min-device-width: 800px)
  and (max-device-width: 1280px)
  and (-webkit-min-device-pixel-ratio: 1.5)
  and (orientation: landscape) {

}

/* ----------- Kindle Fire HD 8.9" ----------- */

/* Portrait and Landscape */
@media only screen
  and (min-device-width: 1200px)
  and (max-device-width: 1600px)
  and (-webkit-min-device-pixel-ratio: 1.5) {

}

/* Portrait */
@media only screen
  and (min-device-width: 1200px)
  and (max-device-width: 1600px)
  and (-webkit-min-device-pixel-ratio: 1.5)
  and (orientation: portrait) {
}

/* Landscape */
@media only screen
  and (min-device-width: 1200px)
  and (max-device-width: 1600px)
  and (-webkit-min-device-pixel-ratio: 1.5)
  and (orientation: landscape) {

}

/*------------------RETINA AND NON RETINA DISPLAYS------------------*/

/* ----------- Non-Retina Screens ----------- */
@media screen
  and (min-device-width: 1200px)
  and (max-device-width: 1600px)
  and (-webkit-min-device-pixel-ratio: 1) {
}

/* ----------- Retina Screens ----------- */
@media screen
  and (min-device-width: 1200px)
  and (max-device-width: 1600px)
  and (-webkit-min-device-pixel-ratio: 2)
  and (min-resolution: 192dpi) {
}

 ```
