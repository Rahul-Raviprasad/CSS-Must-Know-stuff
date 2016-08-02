# CSS-Must-Know-stuff

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
