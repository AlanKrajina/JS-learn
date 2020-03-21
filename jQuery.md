* [Target HTML Elements with Selectors Using jQuery](#Target-HTML-Elements-with-Selectors-Using-jQuery)
* [Target Elements by Class Using jQuery](#Target-Elements-by-Class-Using-jQuery)
* [Target Elements by id Using jQuery](#Target-Elements-by-id-Using-jQuery)
* [Delete Your jQuery Functions](#Delete-Your-jQuery-Functions)
* [Target the Same Element with Multiple jQuery Selectors](#Target-the-Same-Element-with-Multiple-jQuery-Selectors)
* [Remove Classes from an Element with jQuery](#Remove-Classes-from-an-Element-with-jQuery)
* [Change the CSS of an Element Using jQuery](#Change-the-CSS-of-an-Element-Using-jQuery)
* [Disable an Element Using jQuery](#Disable-an-Element-Using-jQuery)
* [Change Text Inside an Element Using jQuery](#Change-Text-Inside-an-Element-Using-jQuery)
* [Remove an Element Using jQuery](#Remove-an-Element-Using-jQuery)
* [Use appendTo to Move Elements with jQuery](#Use-appendTo-to-Move-Elements-with-jQuery)
* [Clone an Element Using jQuery](#Clone-an-Element-Using-jQuery)
* [Target the Parent of an Element Using jQuery](#Target-the-Parent-of-an-Element-Using-jQuery)
* [Target the Children of an Element Using jQuery](#Target-the-Children-of-an-Element-Using-jQuery)
* [Target a Specific Child of an Element Using jQuery](#Target-a-Specific-Child-of-an-Element-Using-jQuery)
* [Target Even Elements Using jQuery](#Target-Even-Elements-Using-jQuery)
* [Use jQuery to Modify the Entire Page](#Use-jQuery-to-Modify-the-Entire-Page)

jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers

https://api.jquery.com/


### Target HTML Elements with Selectors Using jQuery

You should use the jQuery addClass() function to give the classes 'animated' and 'bounce' to your button elements.

`.addClass()`

```
<script>
  $(document).ready(function() {

    $("button").addClass("animated bounce");

  });
</script>

// HTML bellow...
```

### Target Elements by Class Using jQuery

You should use the jQuery addClass() function to give the classes animated and shake to all your elements with the class well.

```
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");              // selector
    $(".well").addClass("animated shake");                // class

  });
</script>
```

### Target Elements by id Using jQuery

```
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");
    $(".well").addClass("animated shake");
    $("#target3").addClass("animated fadeOut");           // id
  });
</script>
```

### Target the Same Element with Multiple jQuery Selectors

```
<script>
  $(document).ready(function() {
    $("button").addClass("animated");
    $(".btn").addClass("shake");
    $("#target1").addClass("btn-primary"); 
  });
</script>
```

### Remove Classes from an Element with jQuery

`.removeClass()`

```
<script>
  $(document).ready(function() {
    $("button").removeClass("btn-default");
  });
</script>
```

### Change the CSS of an Element Using jQuery

`.css()`

```
<script>
  $(document).ready(function() {
    $("#target1").css("color", "red");     // changed color
  });
</script>
```

### Disable an Element Using jQuery

`.prop()`

```
<script>
  $(document).ready(function() {
    $("#target1").prop("disabled", true);    // disabled button with this ID
  });
</script>
```

### Change Text Inside an Element Using jQuery

`.html()`

```
<script>
  $(document).ready(function() {
    $("#target4").html("<em>jQuery Playground</em>");   // changed tags and text
  });
</script>
```

jQuery also has a similar function called `.text()` that only alters text without adding tags. In other words, this function will not evaluate any HTML tags passed to it, but will instead treat it as the text you want to replace the existing content with.

### Remove an Element Using jQuery

`.remove()`

jQuery has a function called `.remove()` that will remove an HTML element entirely

```
<script>
  $(document).ready(function() {
    $("#target4").remove();
  });
</script>
```

### Use appendTo to Move Elements with jQuery

`.appentTo()`

jQuery has a function called `appendTo()` that allows you to select HTML elements and append them to another element.

```
<script>
  $(document).ready(function() {
    $("#target2").appendTo("#right-well");
  });
</script>
```

### Clone an Element Using jQuery

`.clone()`

jQuery has a function called `clone()` that makes a copy of an element.

```
<script>
  $(document).ready(function() {
    $("#target5").clone().appendTo("#left-well");       // chaining methods
  });
</script>
```

### Target the Parent of an Element Using jQuery

`.parent()`

jQuery has a function called `parent()` that allows you to access the parent of whichever element you've selected.

```
<script>
  $(document).ready(function() {
    $("#target1").parent().css("background-color", "red")    // changing target1 PARENT css
  });
</script>
```

### Target the Children of an Element Using jQuery

`.children()`

jQuery has a function called `children()` that allows you to access the children of whichever element you've selected.

```
<script>
  $(document).ready(function() {
    $("#right-well").children().css("color", "orange")        // changing color of #right-well children
  });
</script>
```

### Target a Specific Child of an Element Using jQuery

`target:nth-child(n)`

jQuery uses CSS Selectors to target elements. The `target:nth-child(n)` CSS selector allows you to select all the nth elements with the `target` class or element type.

```
<script>
  $(document).ready(function() {
    $(".target:nth-child(2)").addClass("animated bounce");   // all elements with .target get added a new class (second element)
  });
</script>
```

### Target Even Elements Using jQuery

`:odd` or `:even`

You can also target elements based on their positions using `:odd` or `:even` selectors.

Note that jQuery is zero-indexed which means the first element in a selection has a position of 0. This can be a little confusing as, counter-intuitively, :odd selects the second element (position 1), fourth element (position 3), and so on.


```
<script>
  $(document).ready(function() {
    $(".target:even").addClass("animated shake");     // because indexing FIRST, THIRD shake
    $(".target:odd").addClass("animated shake");
  });
</script>
```

### Use jQuery to Modify the Entire Page

```
<script>
  $(document).ready(function() {
    $("#target1").css("color", "red");
    $("#target1").prop("disabled", true);
    $("#target4").remove();
    $("#target2").appendTo("#right-well");
    $("#target5").clone().appendTo("#left-well");
    $("#target1").parent().css("background-color", "red");
    $("#right-well").children().css("color", "orange");
    $("#left-well").children().css("color", "green");
    $(".target:nth-child(2)").addClass("animated bounce");
    $(".target:even").addClass("animated shake");
    
    $("body").addClass("animated hinge");                 // selecting body
  });
</script>
```
