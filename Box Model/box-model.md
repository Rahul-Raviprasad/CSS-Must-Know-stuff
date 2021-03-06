# Box Model

The content area is that which contains the content.
 The padding area, which is optional and 0 by default, is the area between the content area and the inner edge of the border.
 The border, which is optional and none by default, is the visual edge around an element.
 The margin area, which is optional and 0 by default, is the area outside the border.

Although manipulating the box model affects elements visually, you can never be sure where the boundaries of the content, border, padding, and margin areas are.
A handy little trick is to apply a temporary border around an element to see exactly how it is laid out, by using the following declaration on the element you are working on:
```css
.someClass {
  border: black solid 1px;
}

```

## The Pitfall of the Box Model and Working Around It

Sometime you will find some elements take more space than they should be, when you assign it a width of 100%.
The reason is that, by default, the width of an element is applied only to the content area. so if you have given it some margin, padding and border it would take extra space.

CSS Level 3 introduces the box-sizing property, which allows you to change how the box model works.

## box-sizing

The box-sizing property, which was introduced in CSS3, gives the choice of how you want the box model to work.
The initial value for box-sizing is content-box.
In a nutshell, with box-sizing set to content-box, when you are specifying a width and height, those properties are applied to the content area of an element, and then the padding and border are applied outside those dimensions.

Setting box-sizing to border-box applies padding and borders inside an element with a specified width and height.
