---
title: mi
tags:
  - Markup
  - Elements
  - MathML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mi element indicates that the content should be rendered as an identifier such as function names, variables or symbolic constants. You can also have arbitrary text in it to mark up terms.'
uri: mathml/elements/mi

---
# mi

## Summary

The MathML mi element indicates that the content should be rendered as an identifier such as function names, variables or symbolic constants. You can also have arbitrary text in it to mark up terms.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mi element:

``` {.html}


<math>

  <mi> y </mi>

  <mi> sin </mi>

  <mi mathvariant="monospace"> x </mi>

  <mi mathvariant="bold"> &pi; </mi>

</math>
```

</pre>

## Related specifications

Specification
:   Status
[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mi)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mi)

## Attributes

 mathsize
:   The size of the content. Possible values are:
    -   `small:` Font is rendered smaller than the current font size.
    -   `normal:` Equivalent to 100% or 1em.
    -   `big:` Font is rendered larger than the current font size.
    -   or a custom length.

 mathvariant
:   This logical class of the identifier, which varies in typography. That is, although the names suggest the typographic style for the class, semantically, items with the same class are treated "the same" within an expression, which might or might not involve displaying them with the named typography. The following values are allowed:
    -   `normal` (Default value for *more than one character*)
    -   `bold`
    -   `italic` (Default value for *a single character*)
    -   `bold-italic`
    -   `double-struck`
    -   `bold-fraktur`
    -   `script`
    -   `bold-script`
    -   `fraktur`
    -   `sans-serif`
    -   `bold-sans-serif`
    -   `sans-serif-italic`
    -   `sans-serif-bold-italic`
    -   `monospace`
    -   `initial`
    -   `tailed`
    -   `looped`
    -   `stretched`

