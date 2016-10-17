#Linear Gradient

Linear gradients are defined by an axis, the gradient line, with each point on it being of a different color. Perpendicular lines to the gradient-line have one single color, the one of the point on the gradient line.

The gradient line is defined by the center of the box containing the gradient image and by an angle. The color of the gradient is defined by different points, the starting point, the ending point and, in between, optional stop-color points.

MDN link : https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient

## Using liner gradient to make Image backgrounds dark

We can easily make the background image of pages darker by using following styles
```css
.class {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('http://placehold.it/350x150');  
}
```
View it in codepen
http://codepen.io/RahulRaviprasad/pen/qayKoZ
