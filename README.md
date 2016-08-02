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
