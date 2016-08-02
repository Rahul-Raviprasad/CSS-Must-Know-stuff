### Index
1. Grouping Selectors : using "," comma
2. Descendants: " " space
3. Child: ">" greater than
4. Adjacent Sibling: "+" plus sign, for immediate Sibling
5. General Sibling: "~" tilde sign

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

### Sibling Combinators
CSS Level 3 introduces sibling combinators, allowing you to create selectors for elements when at the same level.

#### Adjacent Sibling Combinator (+)
You can use the adjacent sibling combinator to style elements that share the same parent, providing one element immediately follows the other
```css
p + .offer {
  color: red;
}
```
#### General Sibling Combinator(~)
Like the adjacent sibling combinator, elements making use of the general sibling combinator share the same parent; however, because their relationship is “general,” one element doesn’t have to immediately follow the other to be selected
```css
p ~ h2 {
    color: black;
}
```

note: sibling combinators are unsupported in Internet Explorer 6.
