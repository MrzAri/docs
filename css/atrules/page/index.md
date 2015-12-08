---
title: '@page'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: '@page'
  topic: css
notes:
  - 'Empty "Main Content" section, see @import for notes for improvement suggestion. Remarks section seems to contain all elaboration on the @page rule. By having detail further down it does make for easy quick reference when landing on the page, but can also be confusing to first-time viewers as it differs from the structure of the other rules.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Specifies properties of a page box, such as its dimensions, orientation, and margins. This is used for paged media, such as the printed page.'
tags:
  - CSS_At_Rules
  - CSS
uri: css/atrules/@page

---
<p>
</p>
<h2>Summary</h2>
<p>
Specifies properties of a page box, such as its dimensions, orientation, and margins. This is used for paged media, such as the printed page.</p>
<h2>Examples</h2>
<p>The following are examples of page selectors (declaration block intentionally left blank).
</p>
<div class="example">
<pre class="html">
@page { ... }
@page :left { ... }
@page :right { ... }
@page LandscapeTable { ... }
@page CompanyLetterHead:first { ... } /*  identifier and pseudo page. */
@page:first { ... };

</pre>
<p><br/></p>
</div>
<p>The following are examples of margin boxes where the declaration blocks are intentionally left blank.
</p>
<div class="example">
<pre class="html">
@page {
    @top-left { ... /* document name */ }
    @bottom-center { ... /* page number */}
}

@page :left {
    @left-middle { ... /* page number in left margin */ }
}

@page :right{
    @right-middle { ... /* page number in right margins of right pages */}
}

@page :left {
    @bottom-left-corner { ... /* left page numbers */ }
}

@page :right {
    @bottom-right-corner { ... /* right page numbers */ }
}

@page :first {
    @bottom-left-corner { ... /* empty footer on 1st page */ }
    @bottom-right-corner { ... /* empty footer */ }
}

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<h4>Page Boxes</h4>
<p>In the page model, the document is transferred into one or more page boxes. The page box is a specialized Cascading Style Sheets (CSS) box that maps to a rectangular print media surface.  It is roughly analogous to the viewport.  As for other boxes, a page box consists of margin, border, padding, and content areas. The content and margin areas of a page box have special functions:
</p>
<ul><li>The content area of a page box is called the page area. The content of the document is flowed into the page area. The edges of the page area on the first page establish the rectangle that is the initial containing block of the document.</li>
<li>The margin area of a page box is divided into 16 margin boxes. Each margin box has its own margin, border, padding and content areas. Margin boxed are typically used to display running headers and footers.</li></ul><p>The properties of a page box are determined by properties established within the page context, which is the rule set of the <b>@page</b> rule. Page boxes differ from other boxes in that the <a href="/css/properties/width"><b>width</b></a> and <a href="/css/properties/height"><b>height</b></a> properties do not apply to a page box. The size of the page box is specified using the <b>size</b> property in the page context.
When printing double-sided documents, the page boxes on left and right pages may be different. This can be expressed through CSS pseudo-classes defined in the page context. All pages are automatically classified by user agents into either the <b>:left</b> or <b>:right</b> pseudo-class.
A page that will be on the left if it is part of a pair of facing pages as typically laid out. Page layouts for documents using a left-to-right major writing direction have the earlier of the facing pages on the left. Rules for the left page can be specified using the <b>:left</b> page selector.
A page that will be on the right if it is part of a pair of facing pages as typically laid out. Page layouts for documents using a right-to-left major writing direction have the earlier of the facing pages on the right. Rules for the right page can be specified using the <b>:right</b> page selector.
The first page is generally printed on the front side of a medium. Rules for the first page can be specified using the <b>:first</b> page selector. A first page can be either a left page or a right page, but rules defined for a first page are applied in preference to those defined on a left page or a right page.
</p>
<h4>Margin Boxes</h4>
<p>Margin boxes can be used to create page headers and footers, which are portions of the page set aside for supplementary information such as the page number or document title. The location of page headers and footer is one of the many graphic design choices a document's author makes.
Typically, a page header is located at the top of the page in documents with a predominately horizontal writing direction and on the side opposite the binding edge for documents with a predominately vertical writing direction. One possible design of page headers for horizontally written documents uses the <b>top-left-corner</b>, <b>top-left</b>, <b>top-center</b>, <b>top-right</b>, and <b>top-right-corner</b> margin boxes. Another design, for vertically written documents, could use the <b>right-top</b>, <b>right-middle</b>, and <b>right-bottom</b> margin boxes for right facing pages and <b>left-top</b>, <b>left-middle</b>, and <b>left-bottom</b> for left facing pages. However, there are no constraints placed on the use of margin boxes for page headers.
Typically, the page footer is at the opposite end of the page from the page header. For example, the design of a horizontally written document with a page header at the top of the page could use the <b>bottom-left-corner</b>, <b>bottom-left</b>, <b>bottom-center</b>, <b>bottom-right</b> and <b>bottom-right-corner</b> margin boxes as the page footer. The design of a vertically written document could use the margin boxes of the binding edge of the page for the page footer. However, there are no constraints placed on the use of margin boxes for page footers.
Please note that the margin boxes are oriented with respect to the content and are independent of page orientation, for example the top margin boxes are above the page box in both portrait and landscape orientation.
</p>
<h3>Syntax</h3>
<p><code><b>@page </b><i>page_selector</i><b>?</b> { <b>[</b> <i>page_declaration</i> <b>|</b> <i>margin_ruleset</i> <b>]</b>;<b>*</b> }</code>
<b>page_selector</b>:
<code><i>pageName</i><b>?'</b><i>[<b>:left</b>|<b>:right</b>|<b>:first</b>]'</i><b>?</b></code>
<b>margin_ruleset</b>:
<code>marginBox { <i>margin_declaration</i><b>+</b> }</code>
</p>
<h3>Parameters</h3>
<p>The page name and page pseudo-class constitutes the page selector. The page selector specifies for which pages the declarations apply. In CSS3, page selectors may designate the first page of a document, all left pages, all right pages, or pages with specific names.
</p>
<dl><dt><i>pageName</i></dt>
<dd>Specifies that the declarations in <i>PageContextRules</i> applies to pages with this name. The values "auto" may not be used.</dd>
<dt><code>:left</code></dt>
<dd>Specifies that the declarations in <i>PageContextRules</i> applies to left pages.</dd>
<dt><code>:right</code></dt>
<dd>Specifies that the declarations in <i>PageContextRules</i> applies to right pages.</dd>
<dt><code>:first</code></dt>
<dd>Specifies that the declarations in <i>PageContextRules</i> applies to the first page.</dd></dl><p>The <i>page box</i> contains portions of the document flow destined for rendering on a page sheet. The margins of the page box are divided into <i>margin boxes</i> that act as containing boxes for header/footer content. The area of the page box within its margins form the content area of the page, called the <i>page area</i>.
</p>
<dl><dt><code>marginBox</code></dt>
<dd>Specifies the marginal area that margin declarations apply to. The following marginal areas are defined.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%"><dl><dt>@top-left-corner</dt></dl></td><td width="60%">a fixed-size box filling the area defined by the intersection of the top and left margins of the page box</td></tr><tr><td width="40%"><dl><dt>@top-left</dt></dl></td><td width="60%">a variable-width box within the area defined by the top margin and adjoining the top-left-corner margin box</td></tr><tr><td width="40%"><dl><dt>@top-center</dt></dl></td><td width="60%">a variable-width box within the area defined by the top margin, centered on the page area, and between the top-left and top-right margin boxes</td></tr><tr><td width="40%"><dl><dt>@top-right</dt></dl></td><td width="60%">a variable-width box within the area defined by the top margin and adjoining the top-right-corner margin box</td></tr><tr><td width="40%"><dl><dt>@top-right-corner</dt></dl></td><td width="60%">a box filling the area defined by the intersection of the top and right margins of the page box</td></tr><tr><td width="40%"><dl><dt>@left-top</dt></dl></td><td width="60%">a variable-height box within the area defined by the left margin and adjacent to the bottom of the top-left-corner</td></tr><tr><td width="40%"><dl><dt>@left-middle</dt></dl></td><td width="60%">a variable-height box in the area defined by the left margin, centered on the page area, and between the left-top and left-bottom margin boxes</td></tr><tr><td width="40%"><dl><dt>@left-bottom</dt></dl></td><td width="60%">a variable-height box within the area defined by the left margin and adjacent to the top of the bottom-left-corner</td></tr><tr><td width="40%"><dl><dt>@right-top</dt></dl></td><td width="60%">a variable-height box within the area defined by the right margin and adjacent to the bottom of the top-right-corner</td></tr><tr><td width="40%"><dl><dt>@right-middle</dt></dl></td><td width="60%">a variable-height box in the area defined by the right margin, centered on the page area, and between the right-top and right-bottom margin boxes</td></tr><tr><td width="40%"><dl><dt>@right-bottom</dt></dl></td><td width="60%">a variable-height box within the area defined by the right margin and adjacent to the top of the bottom-right-corner</td></tr><tr><td width="40%"><dl><dt>@bottom-left-corner</dt></dl></td><td width="60%">a box filling the area defined by the intersection of the bottom and left margins of the page box</td></tr><tr><td width="40%"><dl><dt>@bottom-left</dt></dl></td><td width="60%">a variable-width box within the area defined by the bottom margin and adjoining the bottom-left-corner margin box</td></tr><tr><td width="40%"><dl><dt>@bottom-center</dt></dl></td><td width="60%">a variable-width box within the area defined by the bottom margin, centered on the page area, and between the bottom-left and bottom-right margin boxes</td></tr><tr><td width="40%"><dl><dt>@bottom-right</dt></dl></td><td width="60%">a variable-width box within the area defined by the bottom margin and adjoining the bottom-right corner margin box</td></tr><tr><td width="40%"><dl><dt>@bottom-right-corner</dt></dl></td><td width="60%">a box filling the area defined by the intersection of the bottom and right margins of the page box</td></tr></table> </dd>
<dt><i>margin_declaration</i></dt>
<dd>A CSS property declaration applicable to a margin box.</dd>
<dt><i>page_declaration</i></dt>
<dd>A CSS property declaration applicable to the page area.</dd></dl><h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/css3-page/#at-page-rule">CSS Paged Media Module Level 3</a></dt>
  <dd>W3C Working Draft</dd>
</dl><h2>See also</h2>
<h3>Related articles</h3>
<h4>Paged Media</h4>
<ul><li> <strong class="selflink">@page</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/widows">widows</a></li></ul><h4>Syntax</h4>
<ul><li> <a href="/css/atrules/@charset">@charset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/atrules/@font-face">@font-face</a></li></ul><p><br/></p>
<ul><li> <a href="/css/atrules/@import">@import</a></li></ul><p><br/></p>
<ul><li> <a href="/css/atrules/@keyframes">@keyframes</a></li></ul><p><br/></p>
<ul><li> <a href="/css/atrules/@namespace">@namespace</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">@page</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/atrules/@supports">@supports</a></li></ul><p><br/></p>
<ul><li> <a href="/css/reference">CSS reference</a></li></ul><p><br/></p>
<ul><li> <a href="/css/reference/alphabetical">Alphabetical list of CSS reference</a></li></ul><p><br/></p>
<ul><li> <a href="/css/syntax/!important">!important</a></li></ul>
