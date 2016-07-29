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

style sheets in the link tags will still download even if media queries would return(Athough they will not apply)
