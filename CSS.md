* [The CSS Box Model](#The-CSS-Box-Model)
* [CSS Display](#CSS-Display)
* [CSS Layout - The position Property](#CSS-Layout-The-position-Property)
* [CSS Layout - float and clear](#CSS-Layout-float-and-clear)


### The CSS Box Model

The CSS box model is essentially a box that wraps around every HTML element. 
It consists of: 
- Content - The content of the box, where text and images appear
- Padding - Clears an area around the content. The padding is transparent
- Border - A border that goes around the padding and content
- Margin - Clears an area outside the border. The margin is transparent

### CSS Display

- block 
- inline
- none
```
li {
  display: inline;
}

-> Display a list of links as a HORIZONTAL menu:

HTML CSS JavaScript
```

```
li {
  display: block;
}

-> Display a list of links as a VERTICAL menu:

HTML
CSS
JavaScript
```

### CSS Layout - The position Property

https://www.w3schools.com/css/css_positioning.asp

- static
- relative
- fixed
- absolute
- sticky

An element with position: `static`; is not positioned in any special way; it is always positioned according to the normal flow of the page.

An element with position: `relative`; is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.


An element with position: `fixed`; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

An element with position: `absolute`; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

An element with position: `sticky`; is positioned based on the user's scroll position.

A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).

### CSS Layout - float and clear

The CSS `float` property specifies how an element should float.

The CSS `clear` property specifies what elements can float beside the cleared element and on which side.

#### The float Property

The `float` property is used for positioning and formatting content e.g. let an image float left to the text in a container.

The `float` property can have one of the following values:

- left - The element floats to the left of its container
- right - The element floats to the right of its container
- none - The element does not float (will be displayed just where it occurs in the text). This is default
- inherit - The element inherits the float value of its parent
In its simplest use, the float property can be used to wrap text around images.
