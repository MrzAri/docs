---
title: input
tags:
  - Events
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs summary and compat'
uri: dom/Element/input

---
# input

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

## Examples

The following script queries the event [**target**](/dom/Event/target) as the text in a **textArea** is changed.

``` {.js}
<script type="text/javascript">
function handleInput(ev) {
    alert(ev.target.value);
}
window.onload = function() {
    document.getElementById('myTextArea').addEventListener('input',handleInput,false);
}
</script>
<textarea id="myTextArea">Edit this text.</textarea>
```

## Notes

### Remarks

You can use the **oninput** to detect when the contents of a **textArea**, **input type=text**, or **input type=password** have changed. This event occurs immediately after modification, unlike the [**change**](/dom/Element/change) event, which occurs when the element loses focus. To invoke this event, do one of the following:

-   Enter some text into a form field.
-   Cut, delete, or paste content.
-   Navigate to another document.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### External resources

-   [DOM Level 2](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/html.html#ID-6043025)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

