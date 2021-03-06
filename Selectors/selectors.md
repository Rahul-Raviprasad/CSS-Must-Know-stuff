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

### Attribute Selectors
Attribute selectors allow you to select elements by referring to their attributes, such as ID, class, title, src, and so on.
```css
input[type=”text”], input[type=”email”] {
  border: none;
}
```
#### Selecting Elements with an Attribute, Regardless of Its Value

```css
a[title] {
  color: blue;
}
```
#### Selecting Elements with Multiple Attributes
input[type=”submit”][class=”button”] {
  font-size: 1em;
}

## Pseudo-Classes

Sometimes, a part of a web page isn’t made up of a physical element, meaning it can’t be selected through the use of a normal selector; this is where pseudo-classes come in use.

### Dynamic Pseudo-Classes
Dynamic pseudo-classes allow you to style an element when it is interacted with.

A pseudo-class consists of a colon (:) followed by the name of the pseudo-class. Here, you add two pseudo-class rule sets: one for an unvisited link and another for when a user is hov- ering over a link. An unvisited link is underlined, and when hovered over, that underline is removed. When the cursor moves away from the link (and is no longer being hovered over), the underline is applied again.
```css
a:link { /*  An unvisited link */
  text-decoration: underline;
}
a:hover { /*  when you hover over a link */
  text-decoration: none;
}

a:visited {  /*  a link that has been previously visited */
  color: black;
}
a:active { /*  this is when the link is activated, that is you press your mouse down on a link and have not yet released. */
  color: red;
}
/*   Focus is when an interactive element is deemed to have the user’s attention—when an input text box is clicked, for example. With the :focus pseudo-class, you add a very important style: the outline property. It may not seem that important at the moment, but it’s crucial for accessibility. */
a:focus {  /*   */
  outline-color: black;
  outline-style: dotted;
  outline-width: 1px;
}

```
### Structural Pseudo-Classes
Structural pseudo-classes are used when you want to select elements based on generic criteria, such as the second <p> element amongst three.

#### Selecting Child Elements
The pseudo-class :nth-child() allows you to select a particular child element based on its position relative to its siblings within a parent element:
```css
/* this can be either a number or the words odd or even. By selecting only odd or even elements, you can create an alternating color for rows within a table, for example*/
p:nth-child(1) {
  background-color: lightblue;
}
```

nth-child(1) represents the first element, which can also be expressed as :first-child. Similarly, you can use :last-child to select the last element, or if you want to start counting from the last child, you can use :nth-last-child(), where :nth-last- child(1) is the last element and :nth-last-child(2) is the element next to the last.

Selecting Child Elements of a Particular Type
Where :nth-child()selects a child element based on its position among its siblings (regardless of what types of element they are), :nth-of-type() does the same but counts only siblings of the same type:
```css
p:nth-of-type(1) {
  background-color: lightblue;
}
```

#### The Target Pseudo-Class
You are able to place an anchor link on a page that refers to a section on that same page.
If a user clicks on an anchor link, you can style its target to make it stand out, like so:
```css
:target {
  color: red;
}
```

### The UI Element States Pseudo-Classes
The :enabled and :disabled pseudo-classes are used to select elements in enabled and disabled states
:checked, which again relates to input forms

### The Language Pseudo-Class
You can use the :lang pseudo-class to declare styles based on the language of an element. Assume, for example, a quote is in French, like this:
```html
<blockquote>
    <p lang=”fr”>Integer aliquet, lacus in ultricies venenatis,
  eros urna faucibus tellus, sed sollicitudin.</p>
</blockquote>
```
The HTML specifies the quote is of a French language (lang=”fr”). To apply a style to only elements of French language, you can use the following:
```css
:lang(fr) {
  color: blue;
}
```
### The Negation Pseudo-Class
The negation pseudo-class, :not()
eg.
```css
:not(:lang(fr)) {
  color: blue;
}
```
## Pseudo-Elements
Pseudo-elements are parts of a web page that have physical form but aren’t defined by an element—the first line of a paragraph, for example.

Officially, a pseudo-element is made of two colons (::) followed by the name of the element. When you use two colons, pseudo-elements are visually distinguishable from pseudo-classes (with their one colon). However, using one colon is also acceptable, so the choice is yours. I use just one colon. you can generally config this in your linter.

### Selecting the First Line
To select the first line of text, use the pseudo-element :first-line (or ::first-line if you’re going with two colons), like so:
```css
p:first-line {
  font-weight: bold;
}
```
### Selecting the First Letter
```css
#content p:first-of-type:first-letter {
  font-size: 4em;
  font-weight: bold;
}
```
Here, you combine quite a lot of the selectors you’ve learned so far. You use a descendant combinator to select only <p> elements within the <div id=”content” role=”main”> element. You also combine the :first-of-type pseudo-class with :first-letter, which has selected the first element of type <p>, and then select only the :first-letter from that.

### Generating Content Before and After an Element

Sometimes, you might want to add a style before or after an element that doesn’t warrant using another element within the HTML to do that. For this, you can use :before and :after pseudo-elements.
Using :before and :after, add some quotation marks to the customer testimonials:
```css
blockquote p:before {
  content: “\201C”; /*ASCII value for opening quotation marks*/
}
blockquote p:after {
        content: “\201D”;/*ASCII value for closing quotation marks*/
}
```
