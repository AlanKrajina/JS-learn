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

jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.

https://api.jquery.com/


### Target HTML Elements with Selectors Using jQuery

You should use the jQuery addClass() function to give the classes 'animated' and 'bounce' to your button elements.

##### .addClass()

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

##### .removeClass()

```
<script>
  $(document).ready(function() {
    $("button").removeClass("btn-default");
  });
</script>
```

### Change the CSS of an Element Using jQuery

##### .css()

```
<script>
  $(document).ready(function() {
    $("#target1").css("color", "red");     // changed color
  });
</script>
```

### Disable an Element Using jQuery

##### .prop()

```
<script>
  $(document).ready(function() {
    $("#target1").prop("disabled", true);    // disabled button with this ID
  });
</script>
```

### Change Text Inside an Element Using jQuery

### Remove an Element Using jQuery

### Use appendTo to Move Elements with jQuery

### Clone an Element Using jQuery

### Target the Parent of an Element Using jQuery

### Target the Children of an Element Using jQuery

### Target a Specific Child of an Element Using jQuery

### Target Even Elements Using jQuery

### Use jQuery to Modify the Entire Page
