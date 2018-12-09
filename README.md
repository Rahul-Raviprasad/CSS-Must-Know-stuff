# CSS-Must-Know-stuff

## Why This Repository ?
At first glance, CSS looks easy. The first time I changed the color on some text I thought this so easy. Only later on I understood how complicated it can get. We all know different combinations of properties and property values trigger completely different results, or a simple change in one place can completely ruin the entire page.
It made me want to learn CSS properly and to also learn tricks and patterns to help me along. This repository collects some of my stumbling into the common CSS issues, my notes on learning it from different mediums and channels.

## The Role of CSS

The main purpose of CSS is to separate structure (HTML) from presentation (CSS).

By separating structure and presentation, you gain numerous advantages:
• A Cascading Style Sheet can be shared across multiple web pages.
• Sites are easier to maintain and become more flexible.
• The styles applied to a web page can be tailored to suit multiple devices/environments.


## Graceful Degradation

Say you’ve used some of CSS3’s features such as rounded corners and background gradients. An older browser doesn’t understand these features, so it can’t display them. Instead, that browser just shows square corners and a solid background.

In a browser that doesn’t support CSS3, it simply falls back to what it does support. The user of that browser still sees a nicely styled web page and is none the wiser to the fact that in a modern browser, he could be seeing a few extra niceties.

This is generally preferred.

## Progressive enhancement
It starts with an older browser and then later adds new features for modern browsers.

## Link vs import
We can fetch our css files using the "<link>" tag or by using "@import".
Link performs better than import.
Find more here : http://www.stevesouders.com/blog/2009/04/09/dont-use-import/

## Selector Specificity
Quite simply, the most specific selector wins.
This is known as specificity, and it is calculated in a points system, as follows: • Count the number of ID selectors in the selector
• Count the number of class selectors, attribute selectors, and pseudo-classes in the selector
• Count the number of type selectors and pseudo-elements in the selector
• Ignore the universal selector

IDs are deemed to be very specific (because they are unique to the page) and count as 100 points. Each class, attribute, and pseudo-class selector counts as 10 points, and each type or pseudo-element selector counts as 1 point.

What if both rules are as specific as each other?
In this case, the latter rule always wins.
This attribution of importance is known as the cascade—where the C in CSS comes from.
### The !important Rule

The !important rule is ideal during development when you just want to see a style applied to the page, regardless of specificity.
Note try not to use this in production.

## Importance of fake loader before we provide the content
Here is a good article on the same.

# Tricks
1. Reset the user-agent styles using CSS reset
2. Organize your css code using flags
```css
/* ------------------------*/ /* ---------->>> GLOBAL <<<-----------*/ /* ------------------------*/
```
3. Keep a library of helpful CSS classes
4. Separate code into blocks Examples:  Structure , Typography etc.
5. Keep containers to a minimum. “Save your document from structural bloat. New developers will use many div’s similar to table cells to achieve layout. Take advantage of the many structural elements to achieve layout. Do not add more div’s. Consider all options before adding additional wrappers (div’s) to achieve an effect when using a little nifty CSS can get you that same desired effect.” [Ryan Parr]
6. Keep properties to a minimum. “Work smarter, not harder with CSS. Under this rule, there are a number of subrules: if there isn’t a point to adding a CSS property, don’t add it; if you’re not sure why you’re adding a CSS property, don’t add; and if you feel like you’ve added the same property in lots of places, figure out how to add it in only one place.” [CSSing173]
7. Keep selectors to a minimum. “Avoid unnecessary selectors. Using less selectors will mean less selectors will be needed to override any particular style — that means it’s easier to troubleshoot.” [Jonathan Snook68341816]
8. Keep CSS hacks to a minimum. “Don’t use hacks unless its a known and documented bug. This is an important point as I too often see hacks employed to fix things that aren’t really broken in the first place. If you find that you are looking for a hack to fix a certain issue in your design then first do some research (Google is your friend here) and try to identify the issue you are having problems with. [10 Quick Tips for an easier CSS life19]
9. Use CSS Constants for faster development. “The concept of constants – fixed values that can be used through your code [is useful]. [..] One way to get round the lack of constants in CSS is to create some definitions at the top of your CSS file in comments, to define ‘constants’. A common use for this is to create a ‘color glossary’. This means that you have a quick reference to the colors used in the site to avoid using alternates by mistake and, if you need to change the colors, you have a quick list to go down and do a search and replace.” [Rachel Andrew20]
```css
/*
   # Dark grey (text): #333333
   # Dark Blue (headings, links) #000066
   # Mid Blue (header) #333399
   # Light blue (top navigation) #CCCCFF
   # Mid grey: #666666 #
*/
```
10. Name your classes and IDs properly, according to their semantics. “We want to avoid names that imply presentational aspects. Otherwise, if we name something right-col, it’s entirely possible that the CSS would change and our “right-col” would end up actually being displayed on the left side of our page. That could lead to some confusion in the future, so it’s best that we avoid these types of presentational naming schemes.


11. Add Vector Icons to Your Website
Create your icon fonts in seconds. Make your website faster. Over 9,000 icons available.  http://fontastic.me/


Resources:
http://cssreference.io/

Some Inspirations:
http://boombangbong.com/design/textures-web-design-still-relevant/

W3C Homepage for CSS: www.w3.org/Style/CSS
W3C CSS 2.1 Specification: www.w3.org/TR/CSS21
W3C CSS Validator Service: jigsaw.w3.org/css-validator
W3C HTML Validator Service: validator.w3.org
W3C Mobile Web Validator: validator.w3.org/mobile
W3C HTML Home Page: www.w3.org/MarkUp
W3C HTML 4.01 Specification: www.w3.org/TR/html401
W3C XHTML 1.0 Specification: www.w3.org/TR/xhtml1
W3C Mobile Web Best Practices 1.0: www.w3.org/TR/mobile-bp
W3C Accessibility Initiative “HTML 5” Working Group: www.whatwg.org
Mozilla Developer Center: developer.mozilla.org/en/docs

microformats.org
www.alistapart.com
www.simplebits.com/notebook
www.positioniseverything.net
css.maxdesign.com.au
csszengarden.com
meyerweb.com/eric/css
dean.edwards.name/my/cssQuery
addons.mozilla.org/firefox/60
addons.mozilla.org/firefox/179
css-discuss.org
babblelist.com
