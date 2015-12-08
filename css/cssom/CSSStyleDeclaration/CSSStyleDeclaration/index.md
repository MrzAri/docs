---
title: 'CSSStyleDeclaration'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Partially completed tables, could also benefit from examples.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
summary: 'A CSS style declaration which includes properties, values and priorities.'
tags:
  - API_Objects
  - DOM
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/selectors/box-sizing
    - css/properties/ms-flow-from
    - css/properties/ms-flow-into
    - css/properties/ms-grid-column-align
    - css/properties/ms-grid-columns
    - css/properties/ms-grid-row
    - css/properties/ms-grid-row-align
    - css/properties/ms-grid-rows
    - css/properties/ms-grid-row-span
    - css/properties/ms-hyphenate-limit-chars
    - css/properties/ms-hyphenate-limit-zone
    - css/properties/ms-overflow-style
    - css/selectors/-ms-progress-appearance
    - css/properties/ms-scroll-limit
    - css/properties/ms-scroll-limit-yMax
    - css/properties/ms-scroll-limit-xMin
    - css/properties/ms-scroll-limit-xMax
    - css/properties/ms-scroll-limit-yMin
    - css/properties/ms-scroll-chaining
    - dom/properties/scrollLeft
    - dom/properties/scrollTop
    - css/properties/ms-scroll-rails
    - css/properties/ms-scroll-snap-points-x
    - css/properties/ms-scroll-snap-points-y
    - css/properties/ms-scroll-snap-type
    - css/properties/ms-scroll-snap-x
    - css/properties/ms-scroll-snap-y
    - css/properties/ms-scroll-translation
    - css/properties/ms-touch-select
    - css/selectors/-ms-scrollbar-3d-light-color
    - css/selectors/-ms-scrollbar-arrow-color
    - css/selectors/-ms-scrollbar-darkshadow-color
    - css/selectors/-ms-scrollbar-face-color
    - css/selectors/-ms-scrollbar-highlight-color
    - css/selectors/-ms-scrollbar-track-color
uri: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration

---
<p><br/></p>
<h2>Summary</h2>
<p>
A CSS style declaration which includes properties, values and priorities.</p><p><br/></p>
<h2>Properties</h2>

<dl><dt><a href="/css/cssom/CSSStyleDeclaration/cssText">cssText</a></dt>
  <dd>Gets or sets the textual representation of a CSS style declaration.</dd>
</dl><dl><dt><a href="/css/cssom/CSSStyleDeclaration/item">item</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/properties/background">background</a></dt>
  <dd>The background-position property sets the starting position of a background image.</dd>
</dl><dl><dt><a href="/css/cssom/properties/clipBottom">clipBottom</a></dt>
  <dd>Gets the bottom coordinate of the object clipping region.</dd>
</dl><dl><dt><a href="/css/cssom/properties/clipRight">clipRight</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/properties/clipTop">clipTop</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/properties/cssFloat">cssFloat</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/properties/fontWeight">fontWeight</a></dt>
  <dd>Gets or sets the weight of the font of the object.</dd>
</dl><dl><dt><a href="/css/cssom/properties/hasLayout">hasLayout</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/properties/height">height</a></dt>
  <dd>Sets the height of an element.</dd>
</dl><dl><dt><a href="/css/cssom/properties/width">width</a></dt>
  <dd>Sets the width of an element.</dd>
</dl><p><br/></p>
<h2>Methods</h2>

<dl><dt><a href="/css/cssom/CSSStyleDeclaration/getPropertyPriority">getPropertyPriority</a></dt>
  <dd>Gets the priority of a property in a CSS style declaration.</dd>
</dl><dl><dt><a href="/css/cssom/CSSStyleDeclaration/getPropertyValue">getPropertyValue</a></dt>
  <dd>Gets the value of a property in a CSS style declaration.</dd>
</dl><dl><dt><a href="/css/cssom/CSSStyleDeclaration/removeProperty">removeProperty</a></dt>
  <dd>Removes a property from a CSS style declaration.</dd>
</dl><dl><dt><a href="/css/cssom/methods/msGetPropertyEnabled">msGetPropertyEnabled</a></dt>
  <dd>Non standard. Indicates whether a property is enabled.</dd>
</dl><dl><dt><a href="/css/cssom/methods/msPutPropertyEnabled">msPutPropertyEnabled</a></dt>
  <dd>Non standard. Sets a property as enabled or disabled.</dd>
</dl><p><br/></p>
<h2>Events</h2>
<p><i>No events.</i>
</p>

<h2>Notes</h2>
<p>This object may be used to determine the style properties currently set in a block or to set style properties explicitly within the block.
</p>
<h3>Members (MSDN)</h3>
<p>The <b>CSSStyleDeclaration</b> object has these types of members:
</p>
<ul><li><a href="#Additional_Methods">Additional Methods</a></li>
<li><a href="#Additional_Properties">Additional Properties</a></li></ul><p><br/></p>
<h4>Additional Methods</h4>
<p>The <b>CSSStyleDeclaration</b> object has these methods.
</p>
<table class="wikitable"><tr><th>Method
</th>
<th>Description
</th></tr><tr><td><a href="/css/cssom/CSSStyleDeclaration/item"><b>item</b></a>
</td>
<td>Gets a property that has been explicitly set in the current declaration block.
</td></tr></table><p> 
</p>
<h4>Additional Properties</h4>
<p>The <b>CSSStyleDeclaration</b> object has these properties.
</p>
<table class="wikitable"><tr><th>Property
</th>
<th>Description
</th></tr><tr><td><a href="/css/media_queries/accelerator"><b>accelerator</b></a>
</td>
<td>Sets or retrieves a string that indicates whether the object represents a keyboard shortcut.
</td></tr><tr><td><a href="/svg/attributes/alignment-baseline"><b>alignmentBaseline</b></a>
</td>
<td>Specifies which baseline of this element is to be aligned with the corresponding baseline of the parent.
</td></tr><tr><td><a href="/css/properties/animation/animation" class="mw-redirect"><b>animation</b></a>
</td>
<td>Gets or sets one or more shorthand values  that specify all animation properties (except   <a href="/css/properties/animation-play-state"><b>animation-play-state</b></a>) for a set of corresponding object properties  identified in the CSS <a href="/css/atrules/@keyframes"><b>@keyframes</b></a> at-rule specified by the <a href="/css/properties/animation-name"><b>animation-name</b></a> property.
</td></tr><tr><td><a href="/css/properties/animation-delay"><b>animationDelay</b></a>
</td>
<td>Gets or sets one or more values  that specify the offset within an animation cycle (the amount of time from the start of a cycle) before  the animation  is displayed  for a set of corresponding object properties  identified in the CSS <a href="/css/atrules/@keyframes"><b>@keyframes</b></a> at-rule specified by the <a href="/css/properties/animation-name"><b>animation-name</b></a> property.
</td></tr><tr><td><a href="/css/properties/animation-direction"><b>animationDirection</b></a>
</td>
<td>Gets or sets one or more values  that specify the direction of play for an animation cycle.
</td></tr><tr><td><a href="/css/properties/animation-duration"><b>animationDuration</b></a>
</td>
<td>Gets or sets one or more values that specify the length of time to complete one cycle of the animation.
</td></tr><tr><td><a href="/css/properties/animation-fill-mode"><b>animationFillMode</b></a>
</td>
<td>Gets or sets one or more values  that specify whether the effects of an animation are visible before or after it plays.
</td></tr><tr><td><a href="/css/properties/animation-iteration-count"><b>animationIterationCount</b></a>
</td>
<td>Gets or sets one or more values  that specify the number of times an animation cycle is played.
</td></tr><tr><td><a href="/css/properties/animation-name"><b>animationName</b></a>
</td>
<td>Gets or sets a value  that identifies one or more animation names. An animation name identifies (or selects) a  CSS <a href="/css/atrules/@keyframes"><b>@keyframes</b></a> at-rule.
</td></tr><tr><td><a href="/css/properties/animation-play-state"><b>animationPlayState</b></a>
</td>
<td>Gets or sets one or more values  that specify whether an animation is playing or paused.
</td></tr><tr><td><a href="/css/properties/animation-timing-function"><b>animationTimingFunction</b></a>
</td>
<td>Gets or sets one or more values  that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties  identified in the CSS <a href="/css/atrules/@keyframes"><b>@keyframes</b></a> at-rule specified by the <a href="/css/properties/animation-name"><b>animationName</b></a> property.
</td></tr><tr><td><a href="/css/properties/backface-visibility"><b>backfaceVisibility</b></a>
</td>
<td>Gets or sets a value  that specifies whether the back face (reverse side) of an  object is visible.
</td></tr><tr><td><a href="/css/cssom/properties/background"><b>background</b></a>
</td>
<td>Sets or retrieves up to five separate background properties of the object.
</td></tr><tr><td><a href="/css/properties/background-attachment"><b>backgroundAttachment</b></a>
</td>
<td>Sets or retrieves  how the background image is attached to the object within the document.
</td></tr><tr><td><a href="/css/properties/background-clip"><b>backgroundClip</b></a>
</td>
<td>Sets or retrieves the background painting area.
</td></tr><tr><td><a href="/css/properties/background-color"><b>backgroundColor</b></a>
</td>
<td>Sets or retrieves  the color behind the content of the object.
</td></tr><tr><td><a href="/css/properties/background-image"><b>backgroundImage</b></a>
</td>
<td>Sets or retrieves  the background image of the object.
</td></tr><tr><td><a href="/css/properties/background-origin"><b>backgroundOrigin</b></a>
</td>
<td>Sets or retrieves the background positioning area of a box or multiple boxes.
</td></tr><tr><td><a href="/css/properties/background-position"><b>backgroundPosition</b></a>
</td>
<td>Sets or retrieves the position of the background of the object.
</td></tr><tr><td><a href="/css/properties/background-position-x"><b>backgroundPositionX</b></a>
</td>
<td>Sets or retrieves  the x-coordinate of the <a href="/css/properties/background-position"><b>background-position</b></a> property.
</td></tr><tr><td><a href="/css/properties/background-position-y"><b>backgroundPositionY</b></a>
</td>
<td>Sets or retrieves  the y-coordinate of the <a href="/css/properties/background-position"><b>background-position</b></a> property.
</td></tr><tr><td><a href="/css/properties/background-repeat"><b>backgroundRepeat</b></a>
</td>
<td>Sets or retrieves  how the <a href="/css/properties/background-image"><b>background-image</b></a> property of the object is tiled.
</td></tr><tr><td><a href="/css/properties/background-size"><b>backgroundSize</b></a>
</td>
<td>Sets or retrieves the size of the background images.
</td></tr><tr><td><a href="/svg/attributes/baseline-shift"><b>baselineShift</b></a>
</td>
<td>Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
</td></tr><tr><td><a href="/css/media_queries/behavior" class="mw-redirect"><b>behavior</b></a>
</td>
<td>Sets or retrieves  the location of the Dynamic HTML (DHTML) behavior.
</td></tr><tr><td><a href="/css/properties/border"><b>border</b></a>
</td>
<td>Sets or retrieves the properties to draw around the object.
</td></tr><tr><td><a href="/css/properties/border-bottom"><b>borderBottom</b></a>
</td>
<td>Sets or retrieves the properties of the bottom border of the object.
</td></tr><tr><td><a href="/css/properties/border-bottom-color"><b>borderBottomColor</b></a>
</td>
<td>Sets or retrieves  the color of the bottom border of the object.
</td></tr><tr><td><a href="/css/properties/border-bottom-left-radius"><b>borderBottomLeftRadius</b></a>
</td>
<td>Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-left corner for the outer border edge of the current box.
</td></tr><tr><td><a href="/css/properties/border-bottom-right-radius"><b>borderBottomRightRadius</b></a>
</td>
<td>Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-right corner for the outer border edge of the current box.
</td></tr><tr><td><a href="/css/properties/border-bottom-style"><b>borderBottomStyle</b></a>
</td>
<td>Sets or retrieves  the style of the bottom border of the object.
</td></tr><tr><td><a href="/css/properties/border-bottom-width"><b>borderBottomWidth</b></a>
</td>
<td>Sets or retrieves  the width of the bottom border of the object.
</td></tr><tr><td><a href="/css/properties/border-collapse"><b>borderCollapse</b></a>
</td>
<td>Sets or retrieves  a value that indicates whether the row and cell borders of a table are joined in a single border or detached as in standard HTML.
</td></tr><tr><td><a href="/css/properties/border-color"><b>borderColor</b></a>
</td>
<td>Sets or retrieves  the border color of the object.
</td></tr><tr><td><a href="/css/properties/border-left"><b>borderLeft</b></a>
</td>
<td>Sets or retrieves the properties of the left border of the object.
</td></tr><tr><td><a href="/css/properties/border-left-color"><b>borderLeftColor</b></a>
</td>
<td>Sets or retrieves  the color of the left border of the object.
</td></tr><tr><td><a href="/css/properties/border-left-style"><b>borderLeftStyle</b></a>
</td>
<td>Sets or retrieves  the style of the left border of the object.
</td></tr><tr><td><a href="/css/properties/border-left-width"><b>borderLeftWidth</b></a>
</td>
<td>Sets or retrieves  the width of the left border of the object.
</td></tr><tr><td><a href="/css/properties/border-radius"><b>borderRadius</b></a>
</td>
<td>Sets or retrieves one or more values that define the radii of a quarter ellipse that defines the shape of the corners for the outer border edge of the current box.
</td></tr><tr><td><a href="/css/properties/border-right"><b>borderRight</b></a>
</td>
<td>Sets or retrieves the properties of the right border of the object.
</td></tr><tr><td><a href="/css/properties/border-right-color"><b>borderRightColor</b></a>
</td>
<td>Sets or retrieves  the color of the right border of the object.
</td></tr><tr><td><a href="/css/properties/border-right-style"><b>borderRightStyle</b></a>
</td>
<td>Sets or retrieves  the style of the right border of the object.
</td></tr><tr><td><a href="/css/properties/border-right-width"><b>borderRightWidth</b></a>
</td>
<td>Sets or retrieves  the width of the right border of the object.
</td></tr><tr><td><a href="/css/properties/border-spacing"><b>borderSpacing</b></a>
</td>
<td>Sets or retrieves
<p>the distance between the borders of adjoining cells in a table.
</p>
</td></tr><tr><td><a href="/css/properties/border-style"><b>borderStyle</b></a>
</td>
<td>Sets or retrieves  the style of the left, right, top, and bottom borders of the object.
</td></tr><tr><td><a href="/css/properties/border-top"><b>borderTop</b></a>
</td>
<td>Sets or retrieves the properties of the top border of the object.
</td></tr><tr><td><a href="/css/properties/border-top-color"><b>borderTopColor</b></a>
</td>
<td>Sets or retrieves  the color of the top border of the object.
</td></tr><tr><td><a href="/css/properties/border-top-left-radius"><b>borderTopLeftRadius</b></a>
</td>
<td>Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-left corner for the outer border edge of the current box.
</td></tr><tr><td><a href="/css/properties/border-top-right-radius"><b>borderTopRightRadius</b></a>
</td>
<td>Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-right corner for the outer border edge of the current box.
</td></tr><tr><td><a href="/css/properties/border-top-style"><b>borderTopStyle</b></a>
</td>
<td>Sets or retrieves  the style of the top border of the object.
</td></tr><tr><td><a href="/css/properties/border-top-width"><b>borderTopWidth</b></a>
</td>
<td>Sets or retrieves  the width of the top border of the object.
</td></tr><tr><td><a href="/css/properties/border-width"><b>borderWidth</b></a>
</td>
<td>Sets or retrieves  the width of the left, right, top, and bottom borders of the object.
</td></tr><tr><td><a href="/css/properties/bottom"><b>bottom</b></a>
</td>
<td>Sets or retrieves  the bottom position of the object in relation to the bottom of the next positioned object in the document hierarchy.
</td></tr><tr><td><a href="/css/properties/box-shadow"><b>boxShadow</b></a>
</td>
<td>Sets or retrieves a comma-separated list of shadows that attaches one or more drop shadows to the current box.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/box-sizing&amp;action=edit&amp;redlink=1" class="new"><b>boxSizing</b></a>
</td>
<td>Sets or retrieves
<p>the box model to use for object sizing.
</p>
</td></tr><tr><td><a href="/css/properties/break-after"><b>breakAfter</b></a>
</td>
<td>Gets or sets the column-break behavior that follows a content block in a multi-column element.
</td></tr><tr><td><a href="/css/properties/break-before"><b>breakBefore</b></a>
</td>
<td>Gets or sets the column-break behavior that precedes a content block in a multi-column element.
</td></tr><tr><td><a href="/css/properties/break-inside"><b>breakInside</b></a>
</td>
<td>Gets or sets the column-break behavior that occurs within a content block in a multi-column element.
</td></tr><tr><td><a href="/css/properties/caption-side"><b>captionSide</b></a>
</td>
<td>Sets or retrieves
<p>where the <b>caption</b>
of a <a href="/html/elements/table"><b>table</b></a> is located.
</p>
</td></tr><tr><td><a href="/css/properties/clear"><b>clear</b></a>
</td>
<td>Sets or retrieves  whether the object allows floating objects on its left side, right side, or both, so that the next text displays past the floating objects.
</td></tr><tr><td><a href="/css/properties/clip"><b>clip</b></a>
</td>
<td>Sets or retrieves which part of a positioned object is visible.
</td></tr><tr><td><a href="/css/cssom/properties/clipBottom"><b>clipBottom</b></a>
</td>
<td>Gets the bottom coordinate of the object clipping region.
</td></tr><tr><td><a href="/css/cssom/properties/clipLeft"><b>clipLeft</b></a>
</td>
<td>Gets the left coordinate of the object clipping region.
</td></tr><tr><td><a href="/svg/properties/clipPath"><b>clipPath</b></a>
</td>
<td>Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
</td></tr><tr><td><a href="/css/cssom/properties/clipRight"><b>clipRight</b></a>
</td>
<td>Gets the right coordinate of the object clipping region.
</td></tr><tr><td><a href="/svg/attributes/clip-rule"><b>clipRule</b></a>
</td>
<td>Specifies the algorithm used to determine what parts of the canvas are affected by the fill operation.
</td></tr><tr><td><a href="/css/cssom/properties/clipTop"><b>clipTop</b></a>
</td>
<td>Gets the top coordinate of the object clipping region.
</td></tr><tr><td><a href="/css/properties/color"><b>color</b></a>
</td>
<td>Sets or retrieves  the color of the text of the object.
</td></tr><tr><td><a href="/svg/attributes/color-interpolation-filters"><b>colorInterpolationFilters</b></a>
</td>
<td>Specifies which color space to use for filter effects.
</td></tr><tr><td><a href="/css/properties/column-count"><b>columnCount</b></a>
</td>
<td>Gets or sets the optimal number of columns in a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-fill"><b>columnFill</b></a>
</td>
<td>Gets or sets a value that indicates how the column lengths in a multi-column element are affected by the content flow.
</td></tr><tr><td><a href="/css/properties/column-gap"><b>columnGap</b></a>
</td>
<td>Gets or sets the width of the gap between columns in a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-rule"><b>columnRule</b></a>
</td>
<td>Gets or sets a shorthand value  that specifies values for the <a href="/css/properties/column-rule-width"><b>columnRuleWidth</b></a>,  <a href="/css/properties/column-rule-style"><b>columnRuleStyle</b></a>, and the <a href="/css/properties/column-rule-color"><b>columnRuleColor</b></a> of a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-rule-color"><b>columnRuleColor</b></a>
</td>
<td>Gets or sets the color for all column rules in a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-rule-style"><b>columnRuleStyle</b></a>
</td>
<td>Gets or sets the style for all column rules in a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-rule-width"><b>columnRuleWidth</b></a>
</td>
<td>Gets or sets  the width of all column rules in a multi-column element.
</td></tr><tr><td><a href="/css/properties/columns"><b>columns</b></a>
</td>
<td>Gets or sets a shorthand value  that specifies values for the <a href="/css/properties/column-width"><b>column-width</b></a> and the <a href="/css/properties/column-count"><b>column-count</b></a> of a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-span"><b>columnSpan</b></a>
</td>
<td>Gets or sets the number of columns that a content block spans in a multi-column element.
</td></tr><tr><td><a href="/css/properties/column-width"><b>columnWidth</b></a>
</td>
<td>Gets or sets the optimal width of the columns in a multi-column element.
</td></tr><tr><td><a href="/css/properties/content"><b>content</b></a>
</td>
<td>Sets or retrieves
<p>generated content to insert before or after an element.
</p>
</td></tr><tr><td><a href="/css/properties/counter-increment"><b>counterIncrement</b></a>
</td>
<td>Sets or retrieves
<p>a list of counters to increment.
</p>
</td></tr><tr><td><a href="/css/properties/counter-reset"><b>counterReset</b></a>
</td>
<td>Sets or retrieves
<p>a list of counters to create or reset to zero.
</p>
</td></tr><tr><td><a href="/css/cssom/properties/cssFloat"><b>cssFloat</b></a>
</td>
<td>Sets or retrieves a value that specifies whether a box should float to the left, right, or not at all.
</td></tr><tr><td><a href="/css/cssom/styleSheet/cssText"><b>cssText</b></a>
</td>
<td>Sets or retrieves the persisted representation of the style rule.
</td></tr><tr><td><a href="/css/selectors/cursor" class="mw-redirect"><b>cursor</b></a>
</td>
<td>Sets or retrieves  the type of cursor to display as the mouse pointer moves over the object.
</td></tr><tr><td><a href="/css/properties/direction"><b>direction</b></a>
</td>
<td>Sets or retrieves  the reading order of the object.
</td></tr><tr><td><a href="/css/properties/display"><b>display</b></a>
</td>
<td>Gets or sets a value that indicates  whether and how the object is rendered.
</td></tr><tr><td><a href="/svg/attributes/dominant-baseline"><b>dominantBaseline</b></a>
</td>
<td>Sets or retrieves a value that determines or redetermines a scaled-baseline table.
</td></tr><tr><td><a href="/css/properties/empty-cells"><b>emptyCells</b></a>
</td>
<td>Determines whether to show or hide a cell without content.
</td></tr><tr><td><a href="/svg/attributes/enable-background"><b>enableBackground</b></a>
</td>
<td>Allocate a shared background image all graphic elements within a container.
</td></tr><tr><td><a href="/svg/attributes/fill"><b>fill</b></a>
</td>
<td>Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
</td></tr><tr><td><a href="/svg/attributes/fill-opacity"><b>fillOpacity</b></a>
</td>
<td>Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
</td></tr><tr><td><a href="/svg/attributes/fill-rule"><b>fillRule</b></a>
</td>
<td>Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
</td></tr><tr><td><a href="/css/media_queries/filter"><b>filter</b></a>
</td>
<td>Sets or retrieves  the filter or collection of filters that are applied to the object.
</td></tr><tr><td><a href="/svg/properties/filter"><b>filter</b></a>
</td>
<td>The <a href="/svg/properties/filter"><b>filter</b></a> property is generally used to apply a previously define <a href="/svg/elements/filter"><b>filter</b></a> to an applicable element.
</td></tr><tr><td><a href="/svg/attributes/flood-color"><b>floodColor</b></a>
</td>
<td>Specifies the color used to flood the current filter-primitive subregion.
</td></tr><tr><td><a href="/svg/attributes/flood-opacity"><b>floodOpacity</b></a>
</td>
<td>Specifies the opacity value to use with <a href="/svg/elements/feFlood"><b>feFlood</b></a> elements.
</td></tr><tr><td><a href="/css/properties/font"><b>font</b></a>
</td>
<td>Sets or retrieves a combination of separate <a href="/css/properties/font"><b>font</b></a> properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.
</td></tr><tr><td><a href="/css/properties/font-family"><b>fontFamily</b></a>
</td>
<td>Sets or retrieves  the name of the font used for text in the object.
</td></tr><tr><td><a href="/css/properties/font-feature-settings"><b>fontFeatureSettings</b></a>
</td>
<td>Gets or sets one or more values that specify glyph substitution and positioning in fonts that include OpenType layout features.
</td></tr><tr><td><a href="/css/properties/font-size"><b>fontSize</b></a>
</td>
<td>Sets or retrieves  a value that indicates the font size used for text in the object.
</td></tr><tr><td><a href="/css/properties/font-size-adjust"><b>fontSizeAdjust</b></a>
</td>
<td>Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.
</td></tr><tr><td><a href="/css/properties/font-stretch"><b>fontStretch</b></a>
</td>
<td>Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.
</td></tr><tr><td><a href="/css/properties/font-style"><b>fontStyle</b></a>
</td>
<td>Sets or retrieves  the font style of the object as <b>italic</b>, <b>normal</b>, or <b>oblique</b>.
</td></tr><tr><td><a href="/css/fonts/font-variant"><b>fontVariant</b></a>
</td>
<td>Gets or sets  whether the text of the object is in small capital letters.
</td></tr><tr><td><a href="/css/properties/font-weight"><b>fontWeight</b></a>
</td>
<td>Gets of sets  the weight of the font of the object.
</td></tr><tr><td><a href="/svg/attributes/glyph-orientation-horizontal"><b>glyphOrientationHorizontal</b></a>
</td>
<td>Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction  of horizontal.
</td></tr><tr><td><a href="/svg/attributes/glyph-orientation-vertical"><b>glyphOrientationVertical</b></a>
</td>
<td>Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
</td></tr><tr><td><a href="/css/properties/height"><b>height</b></a>
</td>
<td>Sets or retrieves  the height of the object.
</td></tr><tr><td><a href="/css/properties/ime-mode"><b>imeMode</b></a>
</td>
<td>Sets or retrieves the state of an IME.
</td></tr><tr><td><a href="/svg/attributes/kerning"><b>kerning</b></a>
</td>
<td>Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
<p>Gets or sets a value that indicates whether the user-agent should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
</p>
</td></tr><tr><td><a href="/css/properties/layout-flow"><b>layoutFlow</b></a>
</td>
<td>Sets or retrieves  the direction and flow of the content in the object.
</td></tr><tr><td><a href="/css/properties/layout-grid"><b>layoutGrid</b></a>
</td>
<td>Sets or retrieves the composite document grid properties that specify the layout of text characters.
</td></tr><tr><td><a href="/css/properties/layout-grid-char"><b>layoutGridChar</b></a>
</td>
<td>Sets or retrieves  the size of the character grid used for rendering the text content of an element.
</td></tr><tr><td><a href="/css/properties/layout-grid-line"><b>layoutGridLine</b></a>
</td>
<td>Sets or retrieves  the gridline value used for rendering the text content of an element.
</td></tr><tr><td><a href="/css/properties/layout-grid-mode"><b>layoutGridMode</b></a>
</td>
<td>Gets or sets  whether the text layout grid uses two dimensions.
</td></tr><tr><td><a href="/css/properties/layout-grid-type"><b>layoutGridType</b></a>
</td>
<td>Sets or retrieves  the type of grid used for rendering the text content of an element.
</td></tr><tr><td><a href="/css/properties/left"><b>left</b></a>
</td>
<td>Sets or retrieves  the position of the object relative to the left edge of the next positioned object in the document hierarchy.
</td></tr><tr><td><a href="/css/cssom/properties/length"><b>length</b></a>
</td>
<td>Retrieves  the number of properties that  are  explicitly set on the parent object.
</td></tr><tr><td><a href="/css/properties/letter-spacing"><b>letterSpacing</b></a>
</td>
<td>Sets or retrieves  the amount of additional space between letters in the object.
</td></tr><tr><td><a href="/svg/attributes/lighting-color"><b>lightingColor</b></a>
</td>
<td>Defines the color of the light source for filter primitives <a href="/svg/elements/feDiffuseLighting"><b>feDiffuseLighting</b></a>  and <a href="/svg/elements/feSpecularLighting"><b>feSpecularLighting</b></a>.
</td></tr><tr><td><a href="/css/properties/line-break"><b>lineBreak</b></a>
</td>
<td>Deprecated. Gets or sets
<p>line-breaking rules for text in selected languages
such as Japanese, Chinese, and Korean.
</p>
</td></tr><tr><td><a href="/css/properties/line-height"><b>lineHeight</b></a>
</td>
<td>Sets or retrieves  the distance between lines in the object.
</td></tr><tr><td><a href="/css/properties/list-style"><b>listStyle</b></a>
</td>
<td>Sets or retrieves up to three separate <a href="/css/properties/list-style"><b>list-style</b></a> properties of the object.
</td></tr><tr><td><a href="/css/properties/list-style-image"><b>listStyleImage</b></a>
</td>
<td>Sets or retrieves  a value that indicates which image to use as a list-item marker for the object.
</td></tr><tr><td><a href="/css/properties/list-style-position"><b>listStylePosition</b></a>
</td>
<td>Sets or retrieves  a variable that indicates how the list-item marker is drawn relative to the content of the object.
</td></tr><tr><td><a href="/css/properties/list-style-type"><b>listStyleType</b></a>
</td>
<td>Sets or retrieves  the predefined type of the line-item marker for the object.
</td></tr><tr><td><a href="/css/properties/margin"><b>margin</b></a>
</td>
<td>Sets or retrieves  the width of the top, right, bottom, and left margins of the object.
</td></tr><tr><td><a href="/css/properties/margin-bottom"><b>marginBottom</b></a>
</td>
<td>Sets or retrieves  the height of the bottom margin of the object.
</td></tr><tr><td><a href="/css/properties/margin-left"><b>marginLeft</b></a>
</td>
<td>Sets or retrieves  the width of the left margin of the object.
</td></tr><tr><td><a href="/css/properties/margin-right"><b>marginRight</b></a>
</td>
<td>Sets or retrieves  the width of the right margin of the object.
</td></tr><tr><td><a href="/css/properties/margin-top"><b>marginTop</b></a>
</td>
<td>Sets or retrieves  the height of the top margin of the object.
</td></tr><tr><td><a href="/svg/attributes/marker"><b>marker</b></a>
</td>
<td>Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given <a href="/svg/elements/path"><b>path</b></a> element or basic shape.
</td></tr><tr><td><a href="/svg/attributes/marker-end"><b>markerEnd</b></a>
</td>
<td>Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given <a href="/svg/elements/path"><b>path</b></a> element or basic shape.
</td></tr><tr><td><a href="/svg/attributes/marker-mid"><b>markerMid</b></a>
</td>
<td>Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given <a href="/svg/elements/path"><b>path</b></a> element or basic shape.
</td></tr><tr><td><a href="/svg/attributes/marker-start"><b>markerStart</b></a>
</td>
<td>Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given <a href="/svg/elements/path"><b>path</b></a> element or basic shape.
</td></tr><tr><td><a href="/svg/attributes/mask"><b>mask</b></a>
</td>
<td>Sets or retrieves a value that indicates a SVG mask.
</td></tr><tr><td><a href="/css/properties/max-height"><b>maxHeight</b></a>
</td>
<td>Sets or retrieves the maximum height for an element.
</td></tr><tr><td><a href="/css/properties/max-width"><b>maxWidth</b></a>
</td>
<td>Sets or retrieves the maximum width for an element.
</td></tr><tr><td><a href="/css/properties/min-height"><b>minHeight</b></a>
</td>
<td>Sets or retrieves the minimum height for an element.
</td></tr><tr><td><a href="/css/properties/min-width"><b>minWidth</b></a>
</td>
<td>Sets or retrieves the minimum width for an element.
</td></tr><tr><td><a href="/css/properties/ms-block-progression" class="mw-redirect"><b>msBlockProgression</b></a>
</td>
<td>Sets or retrieves the block progression and layout orientation.
</td></tr><tr><td><a href="/css/properties/ms-box-align" class="mw-redirect"><b>msBoxAlign</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-align" class="mw-redirect"><b>-ms-flex-align</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-direction" class="mw-redirect"><b>msBoxDirection</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-flex" class="mw-redirect"><b>msBoxFlex</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex" class="mw-redirect"><b>-ms-flex</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-line-progression" class="mw-redirect"><b>msBoxLineProgression</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-wrap" class="mw-redirect"><b>-ms-flex-wrap</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-lines" class="mw-redirect"><b>msBoxLines</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-wrap" class="mw-redirect"><b>-ms-flex-wrap</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-ordinal-group" class="mw-redirect"><b>msBoxOrdinalGroup</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-order" class="mw-redirect"><b>-ms-flex-order</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-orient" class="mw-redirect"><b>msBoxOrient</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-box-pack" class="mw-redirect"><b>msBoxPack</b></a>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-pack" class="mw-redirect"><b>-ms-flex-pack</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msContentZoomBoundary</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-content-zoom-limit" class="mw-redirect"><b>-ms-content-zoom-limit</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msContentZoomBoundaryMax</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-content-zoom-limit-max" class="mw-redirect"><b>-ms-content-zoom-limit-max</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msContentZoomBoundaryMin</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/css/properties/ms-content-zoom-limit-min" class="mw-redirect"><b>-ms-content-zoom-limit-min</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-chaining" class="mw-redirect"><b>msContentZoomChaining</b></a>
</td>
<td>Gets or sets a value that indicates the zoom behavior that occurs when a user hits the zoom limit during a manipulation.
</td></tr><tr><td><a href="/css/properties/ms-content-zooming" class="mw-redirect"><b>msContentZooming</b></a>
</td>
<td>Gets or sets a value that indicates whether zooming is enabled.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-limit" class="mw-redirect"><b>msContentZoomLimit</b></a>
</td>
<td>Gets or sets a shorthand value  that sets values for the <a href="/css/properties/ms-content-zoom-limit-min" class="mw-redirect"><b>-ms-content-zoom-limit-min</b></a> and the <a href="/css/properties/ms-content-zoom-limit-max" class="mw-redirect"><b>-ms-content-zoom-limit-max</b></a> properties.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-limit-max" class="mw-redirect"><b>msContentZoomLimitMax</b></a>
</td>
<td>Gets or sets a value that specifies the maximum zoom factor.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-limit-min" class="mw-redirect"><b>msContentZoomLimitMin</b></a>
</td>
<td>Gets or sets a value that specifies the minimum zoom factor.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-snap" class="mw-redirect"><b>msContentZoomSnap</b></a>
</td>
<td>Gets or sets a shorthand value  that sets values for the <a href="/css/properties/ms-content-zoom-snap-type" class="mw-redirect"><b>-ms-content-zoom-snap-type</b></a> and the <a href="/css/properties/ms-content-zoom-snap-points" class="mw-redirect"><b>-ms-content-zoom-snap-points</b></a> properties.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-snap-points" class="mw-redirect"><b>msContentZoomSnapPoints</b></a>
</td>
<td>Gets or sets a value that defines where zoom snap-points are located.
</td></tr><tr><td><a href="/css/properties/ms-content-zoom-snap-type" class="mw-redirect"><b>msContentZoomSnapType</b></a>
</td>
<td>Gets or sets a value that indicates how zooming is affected by defined snap-points.
</td></tr><tr><td><a href="/css/properties/ms-flex" class="mw-redirect"><b>msFlex</b></a>
</td>
<td>Gets or sets values that specify the parameters of a flexible length: the positive and negative flexibility, and the preferred size.
</td></tr><tr><td><a href="/css/properties/ms-flex-align" class="mw-redirect"><b>msFlexAlign</b></a>
</td>
<td>Gets or sets a value that specifies the alignment (perpendicular to the layout axis defined by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property) of child elements of the object.
</td></tr><tr><td><a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>msFlexDirection</b></a>
</td>
<td>Gets or sets a value that specifies the display order of  all child elements of the object.
</td></tr><tr><td><a href="/css/properties/ms-flex-flow" class="mw-redirect"><b>msFlexFlow</b></a>
</td>
<td>Gets or sets one or two shorthand values that specify the flex direction and wrap properties together.
</td></tr><tr><td><a href="/css/properties/ms-flex-item-align" class="mw-redirect"><b>msFlexItemAlign</b></a>
</td>
<td>Gets or sets a value that specifies the alignment (perpendicular to the layout axis defined by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property) of child elements of the object.
</td></tr><tr><td><a href="/css/properties/ms-flex-line-pack" class="mw-redirect"><b>msFlexLinePack</b></a>
</td>
<td>Gets or sets a value that specifies how a flexbox's lines align within the flexbox when there is extra space along the axis that is perpendicular to the axis defined by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property.
</td></tr><tr><td><a href="/css/properties/ms-flex-order" class="mw-redirect"><b>msFlexOrder</b></a>
</td>
<td>Gets or sets a value that specifies the ordinal group that a flexbox element belongs to. This ordinal value identifies the  display order for  the group.
</td></tr><tr><td><a href="/css/properties/ms-flex-pack" class="mw-redirect"><b>msFlexPack</b></a>
</td>
<td>Gets or sets a value that specifies how excess space is distributed (along the axis defined by the <a href="/css/properties/ms-flex-direction" class="mw-redirect"><b>-ms-flex-direction</b></a> property) between child elements of the object.
</td></tr><tr><td><a href="/css/properties/ms-flex-wrap" class="mw-redirect"><b>msFlexWrap</b></a>
</td>
<td>Gets or sets a value that specifies whether and in which direction child elements wrap onto multiple lines or columns  based on the space available in the object.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-flow-from&amp;action=edit&amp;redlink=1" class="new"><b>msFlowFrom</b></a>
</td>
<td>Gets or sets a value  that identifies a region container in the document that accepts the content flow from the data source.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-flow-into&amp;action=edit&amp;redlink=1" class="new"><b>msFlowInto</b></a>
</td>
<td>Gets or sets a value  that identifies an <b>iframe</b> container in the document that serves as the region's data source.
</td></tr><tr><td><a href="/css/properties/ms-grid-column" class="mw-redirect"><b>msGridColumn</b></a>
</td>
<td>Gets or sets a value  that specifies in which column of the grid to place the object.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-column-align&amp;action=edit&amp;redlink=1" class="new"><b>msGridColumnAlign</b></a>
</td>
<td>Gets or sets a value  that specifies the horizontal alignment of the object within the  grid column.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-columns&amp;action=edit&amp;redlink=1" class="new"><b>msGridColumns</b></a>
</td>
<td>Gets or sets one or more values that specify the width of each grid column within the object.
</td></tr><tr><td><a href="/css/properties/ms-grid-column-span" class="mw-redirect"><b>msGridColumnSpan</b></a>
</td>
<td>Gets or sets a value  that specifies the number of  columns of the grid that the object spans.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-row&amp;action=edit&amp;redlink=1" class="new"><b>msGridRow</b></a>
</td>
<td>Gets or sets a value  that specifies in which row of the grid to place the object.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-row-align&amp;action=edit&amp;redlink=1" class="new"><b>msGridRowAlign</b></a>
</td>
<td>Gets or sets a value  that specifies the vertical alignment of the object within the  grid row.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-rows&amp;action=edit&amp;redlink=1" class="new"><b>msGridRows</b></a>
</td>
<td>Gets or sets one or more values  that specify the height of each grid row within the object.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-grid-row-span&amp;action=edit&amp;redlink=1" class="new"><b>msGridRowSpan</b></a>
</td>
<td>Gets or sets a value  that specifies the number of  rows of the grid that the object spans.
</td></tr><tr><td><a href="/css/high_contrast_modeapis/properties/ms-high-contrast-adjust"><b>msHighContrastAdjust</b></a>
</td>
<td>Gets or sets a value that indicates whether to override any CSS properties that would have been set in high contrast mode.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-hyphenate-limit-chars&amp;action=edit&amp;redlink=1" class="new"><b>msHyphenateLimitChars</b></a>
</td>
<td>Gets or sets one to three values that indicates the minimum number of characters in a hyphenated word.
</td></tr><tr><td><a href="/css/properties/ms-hyphenate-limit-lines" class="mw-redirect"><b>msHyphenateLimitLines</b></a>
</td>
<td>Gets or sets a value that indicates the maximum number of consecutive lines in an element that may be ended with a hyphenated word.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-hyphenate-limit-zone&amp;action=edit&amp;redlink=1" class="new"><b>msHyphenateLimitZone</b></a>
</td>
<td>Gets or sets a value that defines the width of the hyphenation zone.
</td></tr><tr><td><a href="/css/properties/ms-hyphens" class="mw-redirect"><b>msHyphens</b></a>
</td>
<td>Gets or sets a value that indicates whether additional break opportunities for the current line are created by hyphenating individual words within the line.
</td></tr><tr><td><a href="/css/media_queries/ms-interpolation-mode"><b>msInterpolationMode</b></a>
</td>
<td>Obsolete. Gets or sets the interpolation (resampling) method used to stretch images.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-overflow-style&amp;action=edit&amp;redlink=1" class="new"><b>msOverflowStyle</b></a>
</td>
<td>Gets or sets a value or values that specify the preferred scrolling methods for elements that overflow.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-progress-appearance&amp;action=edit&amp;redlink=1" class="new"><b>msProgressAppearance</b></a>
</td>
<td>This property is obsolete. Use <a href="/css/properties/animation-name"><b>animation-name</b></a> instead.
</td></tr><tr><td><b>msScrollBoundary</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/w/index.php?title=css/properties/ms-scroll-limit&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msScrollBoundaryBottom</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/w/index.php?title=css/properties/ms-scroll-limit-yMax&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-y-max</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msScrollBoundaryLeft</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/w/index.php?title=css/properties/ms-scroll-limit-xMin&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-x-min</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msScrollBoundaryRight</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/w/index.php?title=css/properties/ms-scroll-limit-xMax&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-x-max</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><b>msScrollBoundaryTop</b>
</td>
<td>Do not use. This property has been replaced by the <a href="/w/index.php?title=css/properties/ms-scroll-limit-yMin&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-y-min</b></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-chaining&amp;action=edit&amp;redlink=1" class="new"><b>msScrollChaining</b></a>
</td>
<td>Gets or sets a value that indicates the scrolling behavior that occurs when a user hits the scroll limit during a manipulation.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-limit&amp;action=edit&amp;redlink=1" class="new"><b>msScrollLimit</b></a>
</td>
<td>Gets or sets a shorthand value  that sets values for the <a href="/w/index.php?title=css/properties/ms-scroll-limit-xMin&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-x-min</b></a>, <a href="/w/index.php?title=css/properties/ms-scroll-limit-yMin&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-y-min</b></a>, <a href="/w/index.php?title=css/properties/ms-scroll-limit-xMax&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-x-max</b></a>, and <a href="/w/index.php?title=css/properties/ms-scroll-limit-yMax&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-limit-y-max</b></a> properties.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-limit-xMax&amp;action=edit&amp;redlink=1" class="new"><b>msScrollLimitXMax</b></a>
</td>
<td>Gets or sets a value that specifies the maximum value for the <a href="/w/index.php?title=dom/properties/scrollLeft&amp;action=edit&amp;redlink=1" class="new"><b>scrollLeft</b></a> property.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-limit-xMin&amp;action=edit&amp;redlink=1" class="new"><b>msScrollLimitXMin</b></a>
</td>
<td>Gets or sets a value that specifies the minimum value for the <a href="/w/index.php?title=dom/properties/scrollLeft&amp;action=edit&amp;redlink=1" class="new"><b>scrollLeft</b></a> property.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-limit-yMax&amp;action=edit&amp;redlink=1" class="new"><b>msScrollLimitYMax</b></a>
</td>
<td>Gets or sets a value that specifies the maximum value for the <a href="/w/index.php?title=dom/properties/scrollTop&amp;action=edit&amp;redlink=1" class="new"><b>scrollTop</b></a> property.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-limit-yMin&amp;action=edit&amp;redlink=1" class="new"><b>msScrollLimitYMin</b></a>
</td>
<td>Gets or sets a value that specifies the minimum value for the <a href="/w/index.php?title=dom/properties/scrollTop&amp;action=edit&amp;redlink=1" class="new"><b>scrollTop</b></a> property.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-rails&amp;action=edit&amp;redlink=1" class="new"><b>msScrollRails</b></a>
</td>
<td>Gets or sets a value that indicates whether scrolling will lock to the primary axis of motion.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-snap-points-x&amp;action=edit&amp;redlink=1" class="new"><b>msScrollSnapPointsX</b></a>
</td>
<td>Gets or sets a value that defines where snap-points will be located along the <i>x</i>-axis.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-snap-points-y&amp;action=edit&amp;redlink=1" class="new"><b>msScrollSnapPointsY</b></a>
</td>
<td>Gets or sets a value that defines where snap-points will be located along the <i>y</i>-axis.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-snap-type&amp;action=edit&amp;redlink=1" class="new"><b>msScrollSnapType</b></a>
</td>
<td>Gets or sets a value that  defines what type of snap-point should be used for the current element.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-snap-x&amp;action=edit&amp;redlink=1" class="new"><b>msScrollSnapX</b></a>
</td>
<td>Gets or sets a shorthand value  that sets values for the <a href="/w/index.php?title=css/properties/ms-scroll-snap-type&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-snap-type</b></a> and <a href="/w/index.php?title=css/properties/ms-scroll-snap-points-x&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-snap-points-x</b></a> properties.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-snap-y&amp;action=edit&amp;redlink=1" class="new"><b>msScrollSnapY</b></a>
</td>
<td>Gets or sets a shorthand value  that sets values for the <a href="/w/index.php?title=css/properties/ms-scroll-snap-type&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-snap-type</b></a> and <a href="/w/index.php?title=css/properties/ms-scroll-snap-points-y&amp;action=edit&amp;redlink=1" class="new"><b>-ms-scroll-snap-points-y</b></a> properties.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-scroll-translation&amp;action=edit&amp;redlink=1" class="new"><b>msScrollTranslation</b></a>
</td>
<td>Gets or sets a value that specifies whether vertical-to-horizontal scroll wheel translation occurs on the specified element.
</td></tr><tr><td><a href="/css/properties/ms-touch-action" class="mw-redirect"><b>msTouchAction</b></a>
</td>
<td>Gets or sets a value that indicates whether and how a given region can be manipulated by the user—for instance, by panning or zooming.
</td></tr><tr><td><a href="/w/index.php?title=css/properties/ms-touch-select&amp;action=edit&amp;redlink=1" class="new"><b>msTouchSelect</b></a>
</td>
<td>Gets or sets a value that toggles the "gripper" visual elements that enable touch text selection.
</td></tr><tr><td><a href="/css/exclusions/ms-wrap-flow"><b>msWrapFlow</b></a>
</td>
<td>Gets or sets a value that specifies how exclusions impact inline content within block-level elements.
</td></tr><tr><td><a href="/css/exclusions/ms-wrap-margin"><b>msWrapMargin</b></a>
</td>
<td>Gets or sets a value that is used to offset the inner wrap shape from other shapes.
</td></tr><tr><td><a href="/css/exclusions/ms-wrap-through"><b>msWrapThrough</b></a>
</td>
<td>Gets or sets a value that specifies how content should wrap around an exclusion element.
</td></tr><tr><td><a href="/css/properties/opacity"><b>opacity</b></a>
</td>
<td>Gets or sets a value that specifies object or group opacity in CSS or SVG.
</td></tr><tr><td><a href="/css/properties/orphans"><b>orphans</b></a>
</td>
<td>Sets or retrieves
<p>the minimum number of lines of a paragraph that must appear
at the bottom of a page.
</p>
</td></tr><tr><td><a href="/css/selectors/outline-style" class="mw-redirect"><b>outlineStyle</b></a>
</td>
<td>Sets or retrieves
<p>the style of the outline frame.
</p>
</td></tr><tr><td><a href="/css/properties/overflow"><b>overflow</b></a>
</td>
<td>Sets or retrieves  a value indicating how to manage the content of the object when the content exceeds the height or width of the object.
</td></tr><tr><td><a href="/css/properties/overflow-x"><b>overflowX</b></a>
</td>
<td>Sets or retrieves  how to manage the content of the object when the content exceeds the width of the object.
</td></tr><tr><td><a href="/css/properties/overflow-y"><b>overflowY</b></a>
</td>
<td>Sets or retrieves  how to manage the content of the object when the content exceeds the height of the object.
</td></tr><tr><td><a href="/css/properties/padding"><b>padding</b></a>
</td>
<td>Sets or retrieves the amount of space to insert between the object and its margin or, if there is a border, between the object and its border.
</td></tr><tr><td><a href="/css/properties/padding-bottom"><b>paddingBottom</b></a>
</td>
<td>Sets or retrieves  the amount of space to insert between the bottom border of the object and the content.
</td></tr><tr><td><a href="/css/properties/padding-left"><b>paddingLeft</b></a>
</td>
<td>Sets or retrieves  the amount of space to insert between the left border of the object and the content.
</td></tr><tr><td><a href="/css/properties/padding-right"><b>paddingRight</b></a>
</td>
<td>Sets or retrieves  the amount of space to insert between the right border of the object and the content.
</td></tr><tr><td><a href="/css/properties/padding-top"><b>paddingTop</b></a>
</td>
<td>Sets or retrieves  the amount of space to insert between the top border of the object and the content.
</td></tr><tr><td><a href="/css/properties/page-break-after"><b>pageBreakAfter</b></a>
</td>
<td>Sets or retrieves  a value indicating whether a page break occurs after the object.
</td></tr><tr><td><a href="/css/properties/page-break-before"><b>pageBreakBefore</b></a>
</td>
<td>Sets or retrieves  a string indicating whether a page break occurs before the object.
</td></tr><tr><td><a href="/css/properties/page-break-inside"><b>pageBreakInside</b></a>
</td>
<td>Sets or retrieves
<p>a string indicating whether a page break is allowed to occur inside the
object.
</p>
</td></tr><tr><td><a href="/css/cssom/CSSRule/parentRule"><b>parentRule</b></a>
</td>
<td>Retrieves the containing rule, if the current rule is contained inside another rule.
</td></tr><tr><td><a href="/css/properties/perspective"><b>perspective</b></a>
</td>
<td>Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
</td></tr><tr><td><a href="/css/properties/perspective-origin"><b>perspectiveOrigin</b></a>
</td>
<td>Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an <a href="/css/properties/perspective"><b>perspective</b></a> property declaration.
</td></tr><tr><td><a href="/svg/attributes/pointers"><b>pointerEvents</b></a>
</td>
<td>Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
</td></tr><tr><td><a href="/css/properties/position"><b>position</b></a>
</td>
<td>Sets or retrieves  the type of positioning used for the object.
</td></tr><tr><td><a href="/css/properties/quotes"><b>quotes</b></a>
</td>
<td>Sets or retrieves  the pairs of strings to be used as quotes in generated content.
</td></tr><tr><td><a href="/css/properties/right"><b>right</b></a>
</td>
<td>Sets or retrieves  the position of the object relative to the right edge of the next positioned object in the document hierarchy.
</td></tr><tr><td><a href="/css/properties/ruby-align"><b>rubyAlign</b></a>
</td>
<td>Gets or sets a value that indicates  how to align the ruby text content.
</td></tr><tr><td><a href="/css/properties/ruby-overhang"><b>rubyOverhang</b></a>
</td>
<td>Gets or sets a value that indicates  whether, and on which side, ruby text is allowed to partially overhang any adjacent text in addition to its own base, when the ruby text is wider than the ruby base
</td></tr><tr><td><a href="/css/properties/ruby-position"><b>rubyPosition</b></a>
</td>
<td>Gets or sets  a value that controls the position of the ruby text with respect to its base.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-3d-light-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbar3dLightColor</b></a>
</td>
<td>Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-arrow-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbarArrowColor</b></a>
</td>
<td>Sets or retrieves the color of the arrow elements of a scroll arrow.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-darkshadow-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbarDarkShadowColor</b></a>
</td>
<td>Sets or retrieves the color of the gutter of a scroll bar.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-face-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbarFaceColor</b></a>
</td>
<td>Sets or retrieves the color of the scroll box and scroll arrows of a scroll bar.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-highlight-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbarHighlightColor</b></a>
</td>
<td>Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
</td></tr><tr><td><a href="/css/selectors/-ms-scrollbar-shadow-color" class="mw-redirect"><b>scrollbarShadowColor</b></a>
</td>
<td>Sets or retrieves the color of the bottom and right edges of the scroll box and scroll arrows of a scroll bar.
</td></tr><tr><td><a href="/w/index.php?title=css/selectors/-ms-scrollbar-track-color&amp;action=edit&amp;redlink=1" class="new"><b>scrollbarTrackColor</b></a>
</td>
<td>Sets or retrieves the color of the track element of a scroll bar.
</td></tr><tr><td><a href="/svg/attributes/stop-color"><b>stopColor</b></a>
</td>
<td>Sets or retrieves a value that indicates what color to use at the current gradient stop.
</td></tr><tr><td><a href="/svg/attributes/stop-opacity"><b>stopOpacity</b></a>
</td>
<td>Sets or retrieves a value that defines the opacity of the current gradient stop.
</td></tr><tr><td><a href="/svg/attributes/stroke"><b>stroke</b></a>
</td>
<td>Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
</td></tr><tr><td><a href="/svg/attributes/stroke-dasharray"><b>strokeDasharray</b></a>
</td>
<td>Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
</td></tr><tr><td><a href="/svg/attributes/stroke-dashoffset"><b>strokeDashoffset</b></a>
</td>
<td>Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
</td></tr><tr><td><a href="/svg/attributes/stroke-linecap"><b>strokeLinecap</b></a>
</td>
<td>Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
</td></tr><tr><td><a href="/svg/attributes/stroke-linejoin"><b>strokeLinejoin</b></a>
</td>
<td>Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
</td></tr><tr><td><a href="/svg/attributes/stroke-miterlimit"><b>strokeMiterlimit</b></a>
</td>
<td>Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the <a href="/svg/attributes/stroke-linejoin"><b>strokeLinejoin</b></a> property).
</td></tr><tr><td><a href="/svg/attributes/stroke-opacity"><b>strokeOpacity</b></a>
</td>
<td>Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
</td></tr><tr><td><a href="/svg/attributes/stroke-width"><b>strokeWidth</b></a>
</td>
<td>Sets or retrieves a value that specifies the width of the stroke on the current object.
</td></tr><tr><td><a href="/css/properties/float"><b>styleFloat</b></a>
</td>
<td>Sets or retrieves  on which side of the object the text will flow.
</td></tr><tr><td><a href="/css/properties/table-layout"><b>tableLayout</b></a>
</td>
<td>Sets or retrieves  a string that indicates whether the table layout is fixed.
</td></tr><tr><td><a href="/css/properties/text-align"><b>textAlign</b></a>
</td>
<td>Sets or retrieves  whether the text in the object is left-aligned, right-aligned, centered, or justified.
</td></tr><tr><td><a href="/css/properties/text-align-last"><b>textAlignLast</b></a>
</td>
<td>Gets or sets a value that indicates  how to align the last line or only line of text in the specified object.
</td></tr><tr><td><a href="/svg/attributes/text-anchor"><b>textAnchor</b></a>
</td>
<td>Aligns a string of text relative to the specified point.
</td></tr><tr><td><a href="/css/properties/text-autospace"><b>textAutospace</b></a>
</td>
<td>Sets or retrieves  the autospacing and narrow space width adjustment of text.
</td></tr><tr><td><a href="/css/properties/text-decoration"><b>textDecoration</b></a>
</td>
<td>Sets or retrieves  a value that indicates whether the text in the object has blink, line-through, overline, or underline decorations.
</td></tr><tr><td><a href="/css/properties/text-indent"><b>textIndent</b></a>
</td>
<td>Sets or retrieves  the indentation of the first line of text in the object.
</td></tr><tr><td><a href="/css/properties/text-justify"><b>textJustify</b></a>
</td>
<td>Sets or retrieves  the type of alignment used to justify text in the object.
</td></tr><tr><td><a href="/css/properties/text-kashida-space"><b>textKashidaSpace</b></a>
</td>
<td>Sets or retrieves  the ratio of kashida expansion to white space expansion when justifying lines of text in the object.
</td></tr><tr><td><a href="/css/properties/text-overflow"><b>textOverflow</b></a>
</td>
<td>Sets or retrieves a value that indicates whether to render ellipses (...) to indicate text overflow.
</td></tr><tr><td><a href="/css/properties/text-shadow"><b>text-shadow</b></a>
</td>
<td>Sets or retrieves a comma-separated list of shadows that attaches one or more drop shadows to the specified text.
</td></tr><tr><td><a href="/css/properties/text-transform"><b>textTransform</b></a>
</td>
<td>Sets or retrieves  the rendering of the text in the object.
</td></tr><tr><td><a href="/css/properties/text-underline-position"><b>textUnderlinePosition</b></a>
</td>
<td>Sets or retrieves  the position of the underline decoration that is set through the  <a href="/css/properties/text-decoration"><b>text-decoration</b></a> property of the object.
</td></tr><tr><td><a href="/css/properties/top"><b>top</b></a>
</td>
<td>Sets or retrieves  the position of the object relative to the top of the next positioned object in the document hierarchy.
</td></tr><tr><td><a href="/css/transforms/transform" class="mw-redirect"><b>transform</b></a>
</td>
<td>Gets or sets a list of one or more transform functions that specify how to translate, rotate, or scale an element in 2-D or 3-D space.
</td></tr><tr><td><a href="/css/properties/transform-origin"><b>transformOrigin</b></a>
</td>
<td>Gets or sets one or two values that establish the origin of transformation for an element.
</td></tr><tr><td><a href="/css/properties/transform-style"><b>transformStyle</b></a>
</td>
<td>Gets or sets a value  that specifies how child elements of the object are rendered in 3-D space.
</td></tr><tr><td><a href="/css/properties/transition"><b>transition</b></a>
</td>
<td>Gets or sets one or more shorthand values  that specify the transition properties  for a set of corresponding object properties  identified in the <a href="/css/properties/transition-property"><b>transition-property</b></a> property.
</td></tr><tr><td><a href="/css/properties/transition-delay"><b>transitionDelay</b></a>
</td>
<td>Gets or sets one or more values  that specify the offset within a transition (the amount of time from the start of a transition) before  the transition  is displayed  for a set of corresponding object properties  identified in the <a href="/css/properties/transition-property"><b>transition-property</b></a> property.
</td></tr><tr><td><a href="/css/properties/transition-duration"><b>transitionDuration</b></a>
</td>
<td>Gets or sets one or more values  that specify the durations of transitions on a set of corresponding object properties  identified in the <a href="/css/properties/transition-property"><b>transition-property</b></a> property.
</td></tr><tr><td><a href="/css/properties/transition-property"><b>transitionProperty</b></a>
</td>
<td>Gets or sets a value  that identifies the CSS property name or names to which the transition effect (defined by <a href="/css/properties/transition-duration"><b>transition-duration</b></a>, <a href="/css/functions/transition-timing-function" class="mw-redirect"><b>transition-timing-function</b></a>, and <a href="/css/properties/transition-delay"><b>transition-delay</b></a>) is applied when a new property value is specified.
</td></tr><tr><td><a href="/css/functions/transition-timing-function" class="mw-redirect"><b>transitionTimingFunction</b></a>
</td>
<td>Gets or sets one or more values  that specify the intermediate property values to be used during a transition on a set of corresponding object properties  identified in the <a href="/css/properties/transition-property"><b>transition-property</b></a> property.
</td></tr><tr><td><a href="/css/properties/unicode-bidi"><b>unicodeBidi</b></a>
</td>
<td>Sets or retrieves  the level of embedding with respect to the bidirectional algorithm.
</td></tr><tr><td><a href="/css/properties/vertical-align"><b>verticalAlign</b></a>
</td>
<td>Sets or retrieves  the vertical alignment of the object.
</td></tr><tr><td><a href="/css/properties/visibility"><b>visibility</b></a>
</td>
<td>Sets or retrieves  whether the content of the object is displayed.
</td></tr><tr><td><a href="/css/properties/white-space"><b>whiteSpace</b></a>
</td>
<td>Sets or retrieves a value that indicates whether lines are automatically broken inside the object.
</td></tr><tr><td><a href="/css/properties/widows"><b>widows</b></a>
</td>
<td>Sets or retrieves
<p>the minimum number of lines of a paragraph that must appear
at the top of a document.
</p>
</td></tr><tr><td><a href="/css/properties/width"><b>width</b></a>
</td>
<td>Sets or retrieves  the width of the object.
</td></tr><tr><td><a href="/css/properties/word-break"><b>wordBreak</b></a>
</td>
<td>Sets or retrieves
<p>line-breaking behavior within words, particularly where multiple
languages appear in the object.
</p>
</td></tr><tr><td><a href="/css/text/word-spacing/word-spacing" class="mw-redirect"><b>wordSpacing</b></a>
</td>
<td>Sets or retrieves the amount of additional space between words in the object.
</td></tr><tr><td><a href="/css/properties/word-wrap"><b>wordWrap</b></a>
</td>
<td>Sets or retrieves  whether to break words when the content exceeds the boundaries of its container.
</td></tr><tr><td><a href="/css/properties/writing-mode"><b>writingMode</b></a>
</td>
<td>Sets or retrieves  the direction and flow of the content in the object.
</td></tr><tr><td><a href="/css/properties/z-index"><b>zIndex</b></a>
</td>
<td>Sets or retrieves  the stacking order of positioned objects.
</td></tr><tr><td><a href="/css/selectors/zoom" class="mw-redirect"><b>zoom</b></a>
</td>
<td>Sets or retrieves  the magnification scale of the object.
</td></tr></table><p><br/></p>
<h2>See also</h2>
<h3>Related articles</h3>
<h4>CSSOM</h4>
<ul><li> <a href="/css/cssom/CSSImportRule/href">href</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSImportRule/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule">CSSKeyframeRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule/keyText">keyText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule/style">style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule">CSSKeyframesRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/deleteRule">deleteRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/findRule">findRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/insertRule">insertRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/name">name</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/CSSMediaList">CSSMediaList</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/appendMedium">appendMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/deleteMedium">deleteMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/item">item</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/mediaText">mediaText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/CSSMediaRule">CSSMediaRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/deleteRule">deleteRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/insertRule">insertRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/CSSNamespaceRule">CSSNamespaceRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/namespaceURI">namespaceURI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/prefix">prefix</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSOM_view">CSSOM View</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule">CSSRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/cssText">cssText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/parentStyleSheet">parentStyleSheet</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/type">type</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSStyleDeclaration/getPropertyPriority">getPropertyPriority</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipLeft">clipLeft</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipRight">clipRight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipTop">clipTop</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/cssFloat">cssFloat</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/fontWeight">fontWeight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/hasLayout">hasLayout</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/href">href</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/imports">imports</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/innerWidth">innerWidth</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/isAlternate">isAlternate</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/isPrefAlternate">isPrefAlternate</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/item">item</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/length">length</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/offsetX">offsetX</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/offsetY">offsetY</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/outerHeight">outerHeight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/outerWidth">outerWidth</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageX">pageX</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageXOffset">pageXOffset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageY">pageY</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageYOffset">pageYOffset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pixelBottom">pixelBottom</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/deviceXDPI">deviceXDPI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/deviceYDPI">deviceYDPI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/fontSmoothingEnabled">fontSmoothingEnabled</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/style">style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/style/type">type</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet">styleSheet</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/addImport">addImport</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/blockDirection">blockDirection</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/cssText">cssText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/ownerNode">ownerNode</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/stylesheet/removeImport">removeImport</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/stylesheet/removeRule">removeRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/media_queries/apis/matchMedium">matchMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/getComputedStyle">getComputedStyle</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/innerHeight">innerHeight</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/styleMedia">styleMedia</a></li></ul><p><br/></p><p><br/></p>
<h3>Related pages</h3>
<ul><li><code>IHTMLCSSStyleDeclaration</code></li></ul>
