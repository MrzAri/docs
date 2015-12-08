---
title: 'glyph-orientation-horizontal'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: glyph-orientation-horizontal
  topic: svg
notes:
  - 'Needs all content'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/attributes/glyph-orientation-horizontal

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Notes

### Remarks

This property is applied only to text written in a horizontal [**writingMode**](/css/properties/writing-mode).

The glyph orientation affects the amount that the current text position advances as each glyph is rendered. When the reference orientation direction is horizontal and the **glyphOrientationHorizontal** results in an orientation angle that is a multiple of 180 degrees, the current text position is incremented according to the horizontal metrics of the glyph. Otherwise, if the **glyphOrientationHorizontal** results in an orientation angle that is not a multiple of 180 degrees, the current text position is incremented according to the vertical metrics of the glyph.

### Syntax

    glyph-orientation-horizontal:  angle | inherit

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.7.2

## See also

### Related pages

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**currentStyle**](/css/cssom/currentStyle)
-   [**style**](/css/cssom/style)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextElement**](/svg/elements/text)
-   [**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical)
