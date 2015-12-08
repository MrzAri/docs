---
title: 'The CSS layout model - boxes borders margins padding'
notes:
  - 'Merged into http://docs.webplatform.org/wiki/guides/the_css_layout_model; deletion candidate'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
tags:
  - Tutorials
  - WSC
  - Needs_Summary
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'negativemargins2.html example file'
uri: 'tutorials/The CSS layout model - boxes borders margins padding'

---
<p><br/></p>

<p><br/></p><p><br/></p><p><br/></p>

<h2>Introduction</h2>
<p>At first glance, the CSS layout model is a straightforward affair. Boxes, borders, and margins are fairly simple objects, and CSS syntax provides a simple way to describe their characteristics.
</p><p>However, browser rendering engines follow a long list of rules laid down in the CSS 2.1 Recommendation, and a few of their own. For this reason, there are a lot of details that need to be understood before advanced techniques can be added to a stylist’s repertoire.
</p><p>In this article of the <a rel="nofollow" class="external text" href="http://www.w3.org/wiki/Web_Standards_Curriculum">Web Standards Curriculum</a> you will be introduced to the CSS properties that manipulate the layout of HTML elements, including their borders, margins, and much more. Coverage will also include some of the rules mentioned above. Advanced column layout and grid-focused techniques will be discussed in later articles that will explore form layout, floats, clearing, and positioning in greater detail. There will be many code examples linked to throughout the article to demonstrate techniques discussed, but if you want to work through the code on your local machine, you can <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/article30_examples.zip">download all the code examples here</a>.
</p>
<h2>Changing composition: CSS margins, borders, and padding</h2>
<p>Many HTML elements, such as <code>div</code> elements and headings, are rendered by default to occupy the entire width of the browser canvas and force a terminal linebreak, so that several such elements in series would render in a top-to-bottom stack on the document canvas.
</p><p>However, HTML elements and the browser styles usually set for them are inadequate to the full range of use cases developers are called upon to consider in their work. The way CSS and HTML work together has been tuned to “fill in the gaps” so that <code>class</code>es and <code>id</code>s can add semantic meaning to markup while style sheet rules can precisely change the layout and presentation of content—perhaps even by canceling out large parts of the browser default styles altogether.
</p><p>Careful control of whitespace is among a designer’s most important tools — and in the opinion of this author, the single most important. However, the degree of control over whitespace that brings high production values to a site design is absent from default browser stylesheets, which means that stylists typically make frequent use of the margin, border, padding, and other CSS layout properties explained in this article.
</p><p>Margins, borders, and padding are arranged as shown in Figure 1.
</p><p>
<img alt="how css layout works with margin outside the box and padding inside the box" src="/assets/public/4/44/layout_fig1.png" width="574" height="450"/></p><p>Figure 1: An explicit illustration of the various parts of an element box, labelled with associated CSS properties.
</p>
<h3>Putting whitespace around an object: the margin-top, margin-right, margin-bottom, margin-left, and margin properties</h3>
<p>Margins can be specified singly, or in a shorthand rule. Furthermore, the shorthand rule still allows control of individual borders around an object. Valid values are usually specified in <code>px</code> or <code>em</code> units (pixels or ems). On print-specific stylesheets <code>in</code>, <code>cm</code>, or <code>pt</code> units might be used instead (inches, centimeters or points).
</p><p>In all cases <code>%</code> (percentage) is a valid value, but needs to be used with care; such values are calculated as a proportion of the parent element’s width, and careless provision of values might have unintended consequences. This challenge is explained in more detail during the discussion of the CSS box model below.
</p><p>All inline elements except images lack margins, and will not take margin values. For a list of these elements, consult Table 2 below.
</p>
<h4>auto margins</h4>
<p>Depending upon the circumstances, provision of an <code>auto</code> value instructs the browser to render a margin according to the value provided in its own stylesheet. However, when such a margin is applied to an element with a meaningful width, an <code>auto</code> margin instead causes all of the available space to be rendered as whitespace.
</p><p>Given the following rule:
</p>
<pre>.narrowWaisted {
  width: 16.667em;
  margin: 1em auto 1em auto;
}</pre>
<p>…A block element of the <code>class</code> <code>narrowWaisted</code> will center itself in the middle of the available canvas.
</p><p>…Or the right margin of an applicable element can be set to some relatively small value, while the left margin is assigned an <code>auto</code> value.
</p><p>When that’s done, such an element will instead appear nearly flush-right.
</p>
<h4>Negative margins</h4>
<p>All of the margin properties can be assigned <i>negative</i> values. When this is done, an adjacent margin can be effectively “canceled out” to any degree. Given a large enough negative margin applied to a large enough element, the affected adjacent element can even be <i>overlapped</i>.
</p><p>for example, consider the following simple <code>div</code> elements (taken from <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/negativemargins1.html">example file negativemargin1.html</a>.)
</p>
<pre>&lt;code&gt;&lt;div id="header"&gt;&lt;h1&gt;Lovely header&lt;/h1&gt;&lt;/div&gt;
&lt;div id="content"&gt;&lt;p&gt;Overlapping text is entirely unreadable&lt;/p&gt;&lt;/div&gt;&lt;/code&gt;
</pre>
<p>When styled with the following CSS
</p>
<pre>&lt;code&gt;body {background-color:white; font-family:Geneva, Arial, Helvetica, sans-serif;}
#header { background-color:yellow; }
h1 { color:red;; font-size:2em; }&lt;/code&gt;
</pre>
<p>It creates the output shown in Figure 2:
</p><p>
<img alt="Two elements with no negative margins applied" src="/assets/public/a/ac/layout_fig2.png" width="319" height="118"/></p><p>Figure 2: The two elements from our simple example. Nothing special to see here.
</p><p>Here comes the interesting part. Now we’ll add a fairly sizeable negative margin to the top of the bottom element, using the following rule:
</p>
<pre>&lt;code&gt;#content {margin-top:-3em;}&lt;/code&gt;
</pre>
<p>This gives us the visual effect of shifting the element up so it overlaps with the heading, as shown in Figure 3 (see the <a href="/w/index.php?title=negativemargins2.html_example_file&amp;action=edit&amp;redlink=1" class="new">negativemargins2.html example file</a> for a live example).
</p><p>
<img alt="Two elements with negative margins applied" src="/assets/public/d/dd/layout_fig3.png" width="319" height="119"/></p><p>Figure 3: With a negative margin applied, the bottom element shifts upwards and overlaps the heading.
</p>
<h4>Collapsing margins</h4>
<p>In cases where two similar and adjacent block elements share margins that are greater than zero, only the larger of the two margins will be applied. For example, take the following rule:
</p>
<pre>p {
  margin: 1em auto 1.5em auto;
}
</pre>
<p>If a document including this style rule is rendered <i>literally</i>, the resulting margin between two paragraphs in series wouild be <code>2.5em</code>, as the sum of the bottom margin of paragraph 1 (1.5em) and the top margin of paragraph 2 (1em). However, due to the application of collapsing margins, the margin between them is only <code>1.5em</code>.
</p><p>Lists and headings are peculiar among block elements, so their margins will not be collapsed into the margins of the other block elements.
</p>
<h4>Demonstration 1</h4>
<p>In the text styling article, the typesetting of the opening section of an F. Scott Fitzgerald story was done with many of the tools made available by CSS. For the demonstration in this article, that same page is being put to use again, with some minor changes (principally, the addition of a container element around all of the copy). The text styling is unchanged, but the few layout styles applied to that demonstration have been removed.
</p><p>For starters, margins will be added to all of the elements that will need them.
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev0.html">Minimally styled demonstration document</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_00.css">Beginning stylesheet</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev1.html">New margins on body, title, pullquote, document container, and paragraphs</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_01.css">Demo 1 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>body { margin: 0; }
  #main { margin: 0 auto 0 auto; }
  h1 { margin: 0 0 1em 0; }
  .pullQuote { margin: auto 0 1em 1em; }
  p { margin: 0; }
  .attribution { margin: 0 0 1.5em 0; }
</pre>
<h3>Adding a border to an object: border properties</h3>
<p>There <i>is</i> a <code>border</code> shorthand property, but it’s only useful when you want to provide a complete and consistent border around all four sides of an element. It’s also possible to set the weight (width), style, and colour of any of an element’s four possible borders by using any meaningful combination of the following properties:
</p>
<ul><li> <code>border-width</code></li>
<li> <code>border-style</code></li>
<li> <code>border-color</code></li>
<li> <code>border-top</code></li>
<li> <code>border-top-width</code></li>
<li> <code>border-top-style</code></li>
<li> <code>border-top-color</code></li>
<li> <code>border-right</code></li>
<li> <code>border-right-width</code></li>
<li> <code>border-right-style</code></li>
<li> <code>border-right-color</code></li>
<li> <code>border-bottom</code></li>
<li> <code>border-bottom-width</code></li>
<li> <code>border-bottom-style</code></li>
<li> <code>border-bottom-color</code></li>
<li> <code>border-left</code></li>
<li> <code>border-left-width</code></li>
<li> <code>border-left-style</code></li>
<li> <code>border-left-color</code></li></ul><h4>The border-width properties</h4>
<p>These properties behave exactly as one would expect: they assign explicit weight to one or more borders.
</p><p>The <code>border-width</code> shorthand property accepts values in the same notation as the <code>margin</code> shorthand property, except that percentage values are unsupported. You might well see yourself writing a rule like the following:
</p>
<pre>td {
	border-width: 1px 0 0 1px;
}
</pre>
<h4>The border-style properties</h4>
<p>
<img alt="eight different values for border style in CSS" src="/assets/public/7/71/figure40.png" width="224" height="483"/></p><p>Figure 4: the eight common border styles in action.
</p><p>The <code>border-style</code> properties commonly accept any of the following values:
</p>
<pre> <code>dashed</code> The length of dashes, and the amount of whitespace between them, is determined by the browser. <code>dotted</code> The amount of whitespace between dots (which may take on any shape with an aspect ratio of 1) is determined by the browser. <code>double</code> The provided width will be divided into thirds and rendered in filled-negative-filled order. <code>groove</code> An <code>outset</code> will be rendered immediately inside and flush to an <code>inset</code>. <code>inset</code> The border will be shaded to make it appear as if the element to which it is applied is depressed into the canvas. <code>none</code> Equivalent to specifying a <code>-width</code> of zero. <code>outset</code> The border will be shaded to make it appear as if the element to which it is applied extrudes from the canvas. <code>ridge</code> An <code>inset</code> will be rendered immediately inside and flush to an <code>outset</code>. <code>solid</code> The border appears as an unbroken, unshaded line.  
</pre>
<p>When the <code>border-style</code> shorthand property is used, it can accept up to four values which are applied in the same fashion as <code>margin</code> shorthand values.
</p><p>The practice of obscuring a border (rather than omitting it) is handled by the <code>-color</code> properties.
</p>
<h4>The border-color properties</h4>
<p>Finally, it’s possible to set any color on any individual border, with either a single property such as those listed above, or the <code>border-color</code> shorthand property. Refer to the explanation of the the <code>margin</code> shorthand property for details about the results of providing fewer than four values.
</p><p>Like <code>background-color</code>, <code>border-color</code> can take a value of <code>transparent</code>. This can be useful in dealing with edge cases that require consistent composition but not consistent use of borders.
</p>
<h4>The border shorthand property and its four cousins, in more detail</h4>
<p>Unlike the various <code>-width</code>, <code>-style</code>, and <code>-color</code> border properties, these five properties allow you to define the three characteristics of an object’s four borders, or of any sigle border at a time. Valid <code>border</code> (etc) shorthand values contain any or all of the width, style, and color properties that apply to that border; the only limitation is that you must refer to either one side of an element at a time, or all four at once.
</p><p>Consider the following <code>border</code> rule:
</p>
<pre>#borderShorthandExample {
	border: 2px outset rgb(160,0,0);
	padding: .857em;
	background-color: rgb(255,224,224);
}
</pre>
<p>An element to which the above rule is applied would look exactly like this paragraph.
</p><p>When a value is omitted from a <code>border</code> shorthand rule, the rendered element will display a default result:
</p>
<ul><li> <b>Border width</b> will be determined by the browser.</li>
<li> <b>Border style</b> will be <code>solid</code>.</li>
<li> <b>Border color</b> will be identical to the <code>color</code> applied to the element in question.</li></ul><h4>Creating rules: the rationale for five border shorthand properties… instead of one</h4>
<p>The “rules” discussed here are lines drawn through a layout, not directives to follow. Such lines enhance contrast between an element and its neighbouring space, and in many cases they help to create the illusion of depth within a layout. This last result is exemplified by the existence of the <code>inset</code> and <code>outset</code> border styles.
</p><p>While these same effects can be accomplished by putting borders around all four sides of an element, the ability to draw precisely defined lines in a layout allows its designer considerable control over details.
</p>
<h4>…And why so many properties? They’re just borders, right?</h4>
<p>When a layout is created which demands exceptional skill from a stylist, there will be a need to account for edge cases; this was already raised in the earlier discussion of margins.
</p><p>Because of the way in which site designs are executed, you will encounter many cases where this element or that might have similar structural properties to other elements in a document, but have different presentation requirements. In these situations it makes perfect sense to write one rule for the most common case, and additional rules for each of the edge cases. It’s for this reason that the <code>auto</code> and <code>inherit</code> values exist: to use a default style as an edge case.
</p><p>In the case of borders, edge cases might well require the alteration of a single characteristic of a border on a single side of an element — and when one wisely follows the KISS Principle, it’s usually best to stick to changing <i>only</i> those details which <i>need</i> to be changed.
</p>
<h4>Demonstration 2</h4>
<p>Certain sections of the document should be given embellishment in the form of rules and borders.
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev2.html">Add a bottom rule to the title, and a border around the pullquote</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_02.css">Demo 2 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>h1 { border-bottom: 1px solid rgb(153,153,153); }
.pullQuote { border: 1px solid rgb(153,153,153); }
</pre>
<h3>When margins alone aren’t enough: padding properties</h3>
<p>You will encounter elements with background colours in secondary or accent hues that require gutters between content and margins. In other situations, you’ll need to provide space between borders and the copy near them.
</p><p>In such cases and many others, you’ll get considerable use from the <code>padding</code>, <code>padding-top</code>, <code>padding-right</code>, <code>padding-bottom</code>, and <code>padding-left</code> properties. These properties insert negative space between the margins or borders of an element and its content. See Figure 1 above for a clear illustration of the relationship between margins, borders, and padding.
</p><p>These properties behave in exactly the same manner as margin properties, with the following exceptions:
</p>
<ul><li> <code>auto</code> values are functionally useless in references to padding properties.</li>
<li> Negative padding values are invalid.</li>
<li> Padding is never collapsed.</li>
<li> Margin values are not applied to inline elements, but padding values are.</li></ul><h4>Demonstration 3</h4>
<p>Gutters should be provided for the elements to which borders were previously added.
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev3.html">Insert gutters adjacent to the borders previously put on the title and pullquote</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_03.css">Demo 3 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>body { padding: 0; }
  h1 { padding: .5em 0 .5em 0; }
  .pullQuote { padding: .5em; }
</pre>
<h2>Working with element width and height</h2>
<p>Most elements can have their dimensions altered as a matter of course. You’ve seen this capability demonstrated earlier in this article, during the discussion of <code>auto</code> margins.
</p><p>The CSS properties used to manipulate the dimensions of elements are <code>width</code>, <code>height</code>, <code>min-width</code>, <code>max-width</code>, <code>min-height</code>, and <code>max-height</code>. These properties can then be divorced from (or linked to) the dimensions of element contents with the <code>overflow</code> property.
</p><p>There’s also a <code>clip</code> property which <i>hides</i> parts of an element <i>inside</i> its margins. However, it’s omitted from this article because of its narrow scope of use.
</p>
<h3>width and height basics</h3>
<p>As a rule, <code>width</code> and <code>height</code> produce exactly the results one would expect. However, their use carries some important caveats.
</p>
<ul><li> <b><code>width</code> and <code>height</code> cannot be applied to <code>inline</code> elements…</b> There are several elements (such as <code>span</code>, <code>strong</code>, and <code>em</code>) that will ignore the application of <code>width</code> and <code>height</code> values under typical circumstances. A list of these elements can be found in the discussion of element types, later in this article.</li>
<li> <b>…except for images, which can be assigned <code>width</code> and <code>height</code> even though they are inline elements.</b> The CSS 2.1 Recommendation refers to images as “replaced” elements, which means that the browsers should always treat them as possessing static dimensions.  For this reason, those dimensions can be arbitrarily altered.</li>
<li> <b><code>width</code> and <code>height</code> are only two of the properties that can influence the functional dimensions of an element.</b> As a result, it’s easy to put yourself in situations where an element is too small (usually too narrow) to hold its content as expected, leading to blowouts.  The CSS box model discussion below addresses this issue.</li>
<li> <b>Rendering bugs in Microsoft Internet Explorer (IE) make it necessary to specify explicit <code>width</code> or <code>height</code> property/value pairs for some elements.</b> There are some peculiarities about IE’s rendering engine that can only be resolved with brute force (see the Glossary).  Most of these peculiarities are known and slated to be removed from IE 8, but until that version has replaced its predecessors within the IE install base, this issue will be an inevitable test case.  <a rel="nofollow" class="external text" href="http://www.positioniseverything.net/">PositionIsEverything.net</a> and the <a rel="nofollow" class="external text" href="http://css-discuss.incutio.com/">CSS-Discuss Wiki</a> provide ample information about this issue and techniques that work around it.</li>
<li> <b>Rounding algorithms will, from time to time, cause off-spec differences in layout between browsers which display content via LCD, LED, or CRT (<code>type="screen"</code>) display media.</b> The <code>screen</code> media type ultimately requires all units to be coverted into pixel measurements, which may map differently from one browser to the next.</li></ul><h3>min-width, max-width, min-height, and max-height</h3>
<p>From time to time you will encounter situations in which you need to constrain the size of an element — usually to ensure that a proportionally-sized column will always retain a readable width. The various <code>min-</code> and <code>max-</code> properties answer this requirement. As is the case with <code>width</code> and <code>height</code>, the results one can expect from using these properties are fairly predictable as a matter of course.
</p><p>However, in the experience of this author, these properties have limited use (although other authors disagree). Like plain old <code>width</code> and <code>height</code>, they’re subject to rounding errors that can deliver entirely unexpected results. More importantly, they are completely unsupported in IE 6, which still holds a considerable market share as of July 2008.
</p>
<h4>Demonstration 4</h4>
<p><code>auto</code> margins were placed to the left and right of the page container. Now it needs a <code>width</code> for those margin values to make any sense. Furthermore, the plan is to assign a <code>float</code> value to the pullquote, so that’ll get a width, too.
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev4.html">Change the width of the document container and the pullquote</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_04.css">Demo 4 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>#main { width: 42em; }
.pullQuote { width: 14em; }
</pre>
<h3>overflow: fencing in content, or setting it free</h3>
<p>When an element’s <code>width</code> or <code>height</code> are set, it’s sometimes necessary to consider what results are desired in the event that the contents of that element take up more space than is strictly available. This is especially true on sites with both user generated content and strict layout specifications.
</p><p>The <code>overflow</code> property and its four valid values — <code>visible</code>, <code>hidden</code>, <code>auto</code>, and <code>scroll</code> — are provided to handle such circumstances. Figure 5 illustrates the effect they have when applied to an element whose content spills out of its bounding box.
</p><p>
<img alt="the effects of the CSS overflow property" src="/assets/public/0/02/figure50.png" width="327" height="823"/></p><p>Figure 5: The effects of the CSS overflow property.
</p>
<h4>The results of the four overflow values</h4>
<pre> <code>visible</code> <b>(default)</b> Contents beyond the available dimensions of an element are displayed <i>without</i> affecting the flow or margins of adjacent elements. Consequently, content of one element may appear to <i>collide</i> with the content of its neighbours. Techniques for avoiding this outcome and special cases caused by rendering issues in IE are discussed in later articles. <code>hidden</code> Any content which lies beyond the bounds of an element will be hidden from view. <code>auto</code> The dimensions of an element will be constrained just as when the <code>hidden</code> value is used, except that scrollbars will be created as needed to make overflowing content accessible to the visitor. <code>scroll</code> Both vertical and horizontal scrollbars will be incorporated into the element, even if they’re not needed.  
</pre>
<h2>The CSS box models: fitting everything together</h2>
<p>Now that the fundamental layout properties have been covered, it’s time to discover how the width of an element is rendered by the browser according to its CSS properties — and how to keep elements from blowing out your layouts. Some results will make perfect sense, while others will seem horribly counter-intuitive. To complicate matters, there are actually two layout algorithms to consider: the model specified by the World Wide Web Consortium (W3C) in the CSS 2.1 Recommendation, and the one used in older versions of IE.
</p>
<h3>Choosing the right units for your layout</h3>
<p>As in the case of text, elements can be sized with either proportional units such as <code>%</code> or <code>em</code>, or static units like <code>px</code>. Something else to consider is that the browser canvas is always sized at a static value that cannot be assumed without using client-side script code to either retrieve that size, or resize the window — techniques which are ill-suited to the demands of accessibility, usability, and media portability.
</p>
<h4>The principal rule of sizing elements: mix proportional and static units with care, or not at all</h4>
<p>The default value for both <code>width</code> and <code>height</code> is <code>auto</code>, which in Standard English is a directive to “use the available space.” The result for block elements is that their computed <code>width</code> occupies <i>all</i> of that space. With respect to <code>height</code>, elements expand to enclose their content by default.
</p><p>If you change <code>width</code> and <code>height</code> values, you must then be careful to ensure that the contents of an element will fit (with their margins, borders, and padding) into the width you’ve specified. The easiest way to do this by engaging in the following process:
</p>
<ol><li> Consider the largest maximum width likely to be available for your layout, given common display resolutions and/or type sizes.  As of this writing, this measurement will typically be something around 800 or 1024 pixels.  The broader the expected audience of your site, the more likely it is that the smaller of these values should be chosen.</li>
<li> Create a container element for your entire document that is set to an expected width less than the width worked out in step #1.</li>
<li> Use the same unit type when setting layout properties for the elements within the container element created in step #2.</li></ol><h4>Choosing the right unit type for layout: advantages and disadvantages</h4>
<table border="1"><tr><th>Unit
</th>
<th>Advantages
</th>
<th>Disadvantages
</th></tr><tr><th>em
</th>
<td>
<ul><li> Best suited to creating highly precise layout grids in two dimensions</li>
<li> When used in relation to document containers, makes possible layouts that expand or contract according to the size of body copy</li>
<li> The computed dimensions of elements become easily predictable</li></ul></td>
<td>
<ul><li> Fractional units might expand or contract with slight differences between browsers</li>
<li> To achieve the best results, all <code>font-size</code> and <code>line-height</code> values in the document should be set to explicit and predictable values</li></ul></td></tr><tr><th>percentage
</th>
<td>
<ul><li> Best suited to <i>completely</i> flexible layouts</li>
<li> Easiest for creating things like equal columns</li></ul></td>
<td>
<ul><li> Blowout avoidance might require extra container elements</li>
<li> Might result in unacceptably wide or narrow elements</li>
<li> Results are highly dependent on context (see discussion of the box models below)</li></ul></td></tr><tr><th>px
</th>
<td>
<ul><li> Offers the greatest amount of control over layout</li>
<li> Eliminates most cross-browser variation in layout</li></ul></td>
<td>
<ul><li> Most ill-suited to accessibility and cross-media support requirements</li>
<li> Most susceptible to blowouts</li></ul></td></tr></table><p>Table 1: Advantages and disadvantages of the percentage, em, and pixel units in specifying layout properties.
</p>
<h3>The box model components</h3>
<p>The box model is really just a series of directives that define how the various layout specifications of an element interact with one another. The components covered by the box model are:
</p>
<ol><li> document canvas</li>
<li> margins</li>
<li> borders</li>
<li> padding</li>
<li> element widths and heights</li>
<li> child element properties</li></ol><p>The last of these items in turn includes the other five. However, for simplicity’s sake this section will focus on simple parent-child element relationships, and reserve discussion of multi-level box model interactions for later articles that will delve into the finer points of page layout.
</p>
<h3>The W3C box model: everything is additive</h3>
<p>The basic rule is that the computed width or height of an element is equal to:
</p><p><code>margin + border + padding + (width|height)</code>
</p><p>In many cases the <code>width</code> and/or <code>height</code> will be set to its default value of <code>auto</code>, meaning that the canvas area put aside for content is equal to:
</p><p><code>available_canvas − margin − padding − border</code>
</p><p>In such an equation, <code>available_canvas</code> is itself a discrete (if often auto-computed) value, less the amount of margins, borders and padding. This number is most important for the <i>width</i> of elements, because width calculation errors on the part of a designer will have the undesirable result of causing a horizontal scrollbar to appear in the browser window. Additionally, browsers always place elements at the left margin of the browser canvas that would otherwise overflow beyond the right margin of the browser window, unless instructed to do otherwise.
</p><p>Consider the following style sheet rule:
</p>
<pre>#myLayoutColumn {
  width: 50em;
  margin: 1.5em auto 1.5em auto;
  border: .1em;
  padding: .9em;
}
</pre>
<p>As discussed during the explanation of margin properties above, one can expect <code>#myLayoutColumn</code> to center itself within its container element, whether that container is <code>body</code>, or something created by the production team.
</p><p>Furthermore, if the activation of “strict mode” (through the use of an appropriate <code>!DOCTYPE</code> declaration) causes the W3C box model to be used, one can also expect the computed <i>non-marginal</i> width to be:
</p><p><code>.1em + .9em + 50em + .9em + .1em = 52em</code>
</p><p>In <code>screen</code> media the browser will then take this value, round all of the values separately to the nearest pixel, and render the result accordingly.
</p>
<h4>Proportional margins and padding in the W3C box model</h4>
<p>When the W3C box model is in use, proportional margins and padding are computed relative to the computed <code>width</code> of the <i>containing</i> element. To give one example, if you specify <code>margin: 20%</code> for an element that’s contained within an element that is 800 pixels wide, the margin rendered around the first element will be 160 pixels on all sides (as 20% of 800 is 160).
</p><p>If that same element is assigned <code>padding: 5%</code>, its computed content width will be 400 pixels:
</p>
<pre>&lt;code&gt;20% + 5% + 5% + 20% = ''50%'' ''0.50'' × 800 = ''400''
800 − ''400'' = ''400''&lt;/code&gt;
</pre>
<h2>Working with document flow</h2>
<p>Upcoming tutorials discuss the creation of multi-column layouts, so there are three CSS properties left to introduce in this article: <code>display</code>, <code>float</code>, and <code>clear</code>.
</p>
<h3>Element types and the display property</h3>
<p>With the exception of <code>html</code>, <code>body</code>, and <code>table</code> parts, each element in the HTML 4.01 Recommendation that relates to primary content has an associated type of inline or block. Each type determines default layout behaviour in different ways:
</p>
<h4>Inline</h4>
<ul><li> Text and images that immediately follow and/or precede inline elements are rendered on a common baseline with the content of the inline element, unless they're so long that they would otherwise overlap the edge of the containing element, in which case the inline content will wrap onto a new baseline underneath the first one.</li>
<li> Lines of text within inline elements are laid out with soft linebreaks as needed (or allowed), except where this behaviour is modified by use of the <code>white-space</code> property.</li>
<li> <code>margin</code>, <code>width</code>, <code>height</code>, and <code>float</code> properties in style sheet rules applicable to these elements (except <code>img</code> and <code>object</code>) are ignored.</li>
<li> Inline elements can only contain text or other inline elements.</li></ul><h4>Block</h4>
<ul><li> These elements are rendered as discrete blocks within their containers.</li>
<li> Unless assigned a <code>float</code> value of <code>left</code> or <code>right</code>, will always be rendered with preceding and following linebreaks.</li>
<li> Linebreaks between nested block elements that don’t have any content between them will typically be collapsed.</li>
<li> block elements with a width of <code>auto</code> (the default) will always expand to fill the entire width available to them.</li></ul><p>The <code>display</code> property has three commonly used values — <code>block</code>, <code>inline</code>, and <code>none</code> — of which two refer to the corresponding element types. The effect of changing an element’s <code>display</code> value is to cause an inline element to behave like a block element, to make a block element behave like an inline one, or to alter the rendering of the document as if the element (and all of its contents) did not exist at all.
</p><p>As a matter of course, it’s vital to know which elements correspond to which types by default, relationships laid out briefly in Table 2:
</p>
<table border="1"><tr><th>Element
</th>
<th>Type
</th>
<th>Subtype
</th>
<th>Notes
</th></tr><tr><th><code>a</code>
</th>
<td>inline
</td>
<td>special
</td>
<td> 
</td></tr><tr><th><code>abbr</code>
</th>
<td>inline
</td>
<td>phrase
</td>
<td> 
</td></tr><tr><th><code>acronym</code>
</th>
<td>inline
</td>
<td>phrase
</td>
<td> 
</td></tr><tr><th><code>address</code>
</th>
<td>block
</td>
<td> 
</td>
<td>Behaves similarly to <code>p</code> in common practice
</td></tr><tr><th><code>blockquote</code>
</th>
<td>block
</td>
<td> 
</td>
<td>Must contain at least one block element when the declared <code>!DOCTYPE</code> is <code>Strict</code>
</td></tr><tr><th><code>body</code>
</th>
<td> 
</td>
<td> 
</td>
<td>Encloses the entire document canvas; commonly takes on a margin (in IE, Firefox, and Safari) or padding (in Opera) of <code>10px</code> in <code>screen</code> media
</td></tr><tr><th><code>cite</code>
</th>
<td>inline
</td>
<td>phrase
</td>
<td> 
</td></tr><tr><th><code>div</code>
</th>
<td>block
</td>
<td> 
</td>
<td> 
</td></tr><tr><th><code>em</code>
</th>
<td>inline
</td>
<td>phrase
</td>
<td> 
</td></tr><tr><th><code>fieldset</code>
</th>
<td>block
</td>
<td> 
</td>
<td>Commonly rendered by default with <code>border: 1px black;</code>
</td></tr><tr><th><code>form</code>
</th>
<td>block
</td>
<td> 
</td>
<td> 
</td></tr><tr><th><code>h1 … h6</code>
</th>
<td>block
</td>
<td>heading
</td>
<td> 
</td></tr><tr><th><code>input</code>
</th>
<td>inline
</td>
<td>formctrl
</td>
<td> 
</td></tr><tr><th><code>img</code>
</th>
<td>inline
</td>
<td>special
</td>
<td> 
</td></tr><tr><th><code>label</code>
</th>
<td>inline
</td>
<td>formctrl
</td>
<td> 
</td></tr><tr><th><code>li</code>
</th>
<td>block
</td>
<td> 
</td>
<td>Element type not specified in Document Type Definition, but this element may contain either block or inline elements; the complete CSS 2.1 Recommendation sets aside a <code>display</code> value for list items
</td></tr><tr><th><code>ol</code>
</th>
<td>block
</td>
<td>list
</td>
<td> 
</td></tr><tr><th><code>p</code>
</th>
<td>block
</td>
<td> 
</td>
<td>May only contain inline elements; commonly rendered with top and bottom margins
</td></tr><tr><th><code>span</code>
</th>
<td>inline
</td>
<td>special
</td>
<td> 
</td></tr><tr><th><code>strong</code>
</th>
<td>inline
</td>
<td>phrase
</td>
<td> 
</td></tr><tr><th><code>table</code>
</th>
<td>block
</td>
<td> 
</td>
<td> 
</td></tr><tr><th><code>ul</code>
</th>
<td>block
</td>
<td>list
</td>
<td> 
</td></tr></table><p>Table 2: Frequently used HTML elements and their types. Only margins between two adjacent block elements of the same subtype will collapse.
</p>
<h4>Demonstration 5</h4>
<p>How about removing the “Prologue” annotation from the title, just for demonstration’s sake?
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev5.html">Remove the extraneous bit from the title</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_05.css">Demo 5 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>.sectionNote { display: none; }
</pre>
<h3>Causing elements to flow around others: the float property</h3>
<div class="floatleft"><img alt="a cat with bacon taped to his back" src="/assets/public/4/4e/box_baco.jpg" width="240" height="158"/></div>
<p>A photo is positioned to the left of this paragraph. Practically all of you will see that the following copy flows naturally <i>around</i> it, though some might need first to cease wondering why a well-known science fiction novelist would tape bacon to his cat—even if he was having a slow day. HTML attributes can be used to specify the layout behaviour you see, but in this instance the results were accomplished with CSS.
</p><p>As one can imagine, the property/value pair that works this magic is <code>float: left;</code>. The finer points of working with floats will be addressed in later articles, but it’s necessary to touch on the basics here. <code>float: right</code> is also a perfectly serviceable property/value pair, and for those occasions when you need to contradict a <code>class</code> assignment that invokes <code>float</code>, you can specify <code>float: none</code>.
</p><p>The <code>float</code> property <i>does</i> come with a few use instructions:
</p>
<ul><li> A <code>float</code> value will only matter if it’s applied to a block element with an explicit <code>width</code>.</li>
<li> <code>float</code>, <code>clear</code>, and <code>margin</code> properties all appear <i>together</i> in style sheet rules meant to create columns within a layout.</li>
<li> Causing a floated element to stretch to the bottom of its container is a tricky matter, but not impossible. The common way to do this is referred to as <a rel="nofollow" class="external text" href="http://www.alistapart.com/articles/fauxcolumns/">faux-columns</a>.</li></ul><h4>Demonstration 6</h4>
<p>Placement of a <code>float</code> value on the pullquote has been talked about, so now it gets done and the results can be seen. While we're at it, let's add some background colour to help distinguish it from the main content.
</p>
<h5>Links:</h5>
<ul><li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev6.html">Float the pullquote over at the right margin</a></li>
<li> <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_06.css">Demo 6 stylesheet</a></li></ul><h5>New rules:</h5>
<pre>.pullQuote { float: right;
background-color: rgb(204,204,204); }
</pre>
<h3>Forcing elements below their floated predecessors: the clear property</h3>
<p>Like the <code>float</code> property, the <code>clear</code> property can be assigned one of the <code>left</code>, <code>right</code>, or <code>none</code> values. The <code>both</code> value is also supported.
</p><p>While the <code>float</code> property directs how the content of subsequent elements should flow around it, the <code>clear</code> property directs how an element should flow around all of its neighbours—in many practical cases, not at all.
</p><p>Figure 6 illustrates the behaviour of <code>clear: left;</code> in a layout where two initial consecutive elements have been assigned identical <code>height</code> values, and <code>float</code> values of <code>left</code> and <code>right</code>:
</p><p>
<img alt="clear left allows the bottom box to clear both columns as they are the same height" src="/assets/public/e/e6/figure60.png" width="545" height="434"/></p><p>Figure 6: <code>clear:left </code> allows the bottom box to clear both columns, as they are the same height.
</p><p>In the preceding demonstration, the <i>default</i> flow of <code>#cLeftWidget</code> would place it just below the Latin text — that is, <i>between</i> <code>#fLeftWidget</code> and <code>#fRightWidget</code>.
</p><p>Consider what happens when the first of the same collection of elements is made shorter than its flush-right sibling, as seen in Figure 7.
</p><p>
<img alt="When the right column is longer than the left column clear left will not clear both columns and so clear both must be used instead" src="/assets/public/6/61/figure70.png" width="542" height="369"/></p><p>Figure 7: When the right column is longer than the left column, <code>clear:left </code> will not clear both columns and so <code>clear:both </code> must be used instead
</p><p>In the first example, the <code>clear</code> value of the trailing element is set to <code>left</code> in order to make a point: because both of the <code>float</code>ed elements are the same height, the <code>clear</code>ed element will be pushed below both. However, the second example proves that in order to achieve the same result with <code>float</code>ed elements of differing heights, <code>clear: both;</code> must be used.
</p><p>This discussion of the <code>clear</code> property is intended as a simple introduction to its effects, while later articles discuss the finer points of technique associated with its use.
</p>
<h2>Summary</h2>
<p>Between differences in rendering engines, the need to cover a wide swathe of traditionally defined ground, and the inability to predict the certain dimensions of a browser window, the layout of Web documents is fraught with hassles and caveats. However, the common level of CSS support has advanced to the point where Web documents are not hard to get to give decent results across browsers.
</p>
<h2>Further reading</h2>
<ul><li> Bergevin, Holly, and Gallant, John. 2006. <a rel="nofollow" class="external text" href="http://positioniseverything.net/explorer.html">Explorer exposed</a>. Position Is Everything. (accessed 1 July 2008).</li>
<li> Bos, Bert, <i>et al.</i> 2007. <a rel="nofollow" class="external text" href="http://www.w3.org/TR/2007/CR-CSS21-20070719">Cascading style sheets level 2 revision 1 (CSS 2.1) specification</a>. World Wide Web Consortium. <i>etc.</i> (accessed 30 June 2008).</li>
<li> Raggett, Dave, <i>et. al</i>. 1999. <a rel="nofollow" class="external text" href="http://www.w3.org/TR/1999/REC-html401-19991224">HTML 4.01 specification</a>. World Wide Web Consortium. <i>etc.</i> (accessed 30 June 2008).</li>
<li> Raymond, Eric, and Steele, Guy, eds. 2003. <a rel="nofollow" class="external text" href="http://www.catb.org/jargon/html/B/brute-force.html">Brute force</a>. The Jargon File (Version 4.4.7). (accessed 30 June 2008).</li>
<li> Scalzi, John. 2006. <a rel="nofollow" class="external text" href="http://www.scalzi.com/whatever/004457.html">Clearly you people thought I was kidding</a>. Whatever. (accessed 30 June 2008).</li></ul><h2>Exercise questions</h2>
<ol><li> Under which circumstances is it best to use the shorthand <code>margin</code> value, or a single margin property such as <code>margin-top</code>?</li>
<li> When the shorthand <code>margin</code>, <code>padding</code>, and <code>border-width</code> properties are provided with all four values, in what order are those values applied to the four sides of an element?</li>
<li> If you want to place a rule under the text of each heading in a document, which property would you use?</li>
<li> Which <code>border-style</code> value would you use to give an element an appearance like an interface button?</li>
<li> <i>Yes or no:</i> Will specifying a border around an element will also provide for a gutter around the content of that element, by default?</li>
<li> If you create an element that isn’t as wide as its container, which property/value pair do you need to set to ensure that the element is horizontally centered within its container?</li>
<li> <i>Yes or no:</i> If you place a container element within <code>body</code> and set its <code>width</code> to a value greater than <code>100%</code>, will the behaviour of the document canvas change?</li>
<li> If an image is too large for its containing element, which property/value pair would you use to ensure that your page layout doesn’t blow out, and why?</li>
<li> If you assign a <code>display</code> value of <code>block</code> to an <code>a</code> (link) element and give that element a reasonable height and width, how does the mouseover behaviour of that link change in <code>screen</code> display media?</li>
<li> Under normal circumstances, a block element expands to fill the width of its container (less margins, borders, and padding). By default, does this behaviour truly change when that element is preceded by a <code>float</code>ed element — or merely <i>appear</i> to change?</li>
<li> If you intend to apply a <code>float</code> value to an element, which other property must you also set on that element?</li>
<li> If you wanted to make <i>absolutely</i> sure that an element would <i>always</i> expand to fill the width of its container, which property/value pairs would you set?</li></ol><p>Note: This material was originally published as part of the Opera Web Standards Curriculum, available as <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/">30: The CSS layout model - boxes, borders, margins, padding</a>, written by Ben Henick. Like the original, it is published under the <a rel="nofollow" class="external text" href="http://creativecommons.org/licenses/by-nc-sa/2.5/">Creative Commons Attribution, Non Commercial - Share Alike 2.5</a> license.
</p>
