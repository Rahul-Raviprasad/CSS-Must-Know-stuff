## Grouping Selectors
we can simply group many selectors together by the use of commas
```css
h1, h2, h3, h4 {
  color: green;
}
```
## Combinators
Combinators allow you to apply styles to elements based on their relationship with other elements.

### Descendant Combinators
A descendant selector describes the descendant of an element. Descendant combinators are great for styling elements that exist inside of other elements.
```css
div p {
  font-size: 2em; /* All p descendants of div will be made 2em */
}
```
### Child Combinators
Sometimes, a descendant combinator isn’t quite strict enough for your purposes. use the ">" greater than symbol to apply style to immediate children.
```css
aside > h3 {
  font-weight: bold;
}
```
note : Child combinators are unsupported in Internet Explorer 6.
