{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent,  Children information and HTML information subsection. Complete Compatibility table.
|Checked_Out=Yes
|High-level issues=Needs Review
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Control which image resource a user agent presents to a user, based on media query and/or support for a particular image format.}}
{{Markup_Element
|DOM_interface=dom/HTMLPictureElement
|Content=The '''picture''' element (<code><picture></code>) addresses use cases that are left unaddressed by the srcset attribute, the most important being art direction. 

Other use cases, such as matching media features and media types and matching on supported image formats, are also addressed by this element.

===Attributes===

This element supports the HTML5 [[html/global_attributes|global attributes]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description='''Art direction use case::''' This example shows the basic usage of the picture element for responsive images and art direction.
|Code=<picture>
  &lt;source media="(min-width: 650px)" srcset="images/kitten-large.png">
  &lt;source media="(min-width: 465px)" srcset="images/kitten-medium.png">
  &lt;!-- img tag for browsers that do not support picture element -->
  <img src="images/kitten-small.png" alt="a cute kitten">
</picture>
|LiveURL=http://googlechrome.github.io/samples/picture-element/
}}{{Single Example
|Language=HTML
|Description='''Different image types use case:''' Browsers that support WebP get a WebP image; other browsers get JPG.
|Code=<picture>
  &lt;source
    srcset="opera.webp"
    type="image/webp">
    <img
      src="opera.jpg" alt="The Oslo Opera House">
</picture>
}}{{Single Example
|Language=HTML
|Description='''High-DPI images & art direction use case:''' For browser windows with a width of 1024 CSS pixels and wider, a full-shot photo is used; smaller browser windows get a close-up photo. In addition, these photos are served as high-resolution images to browsers on devices with high-DPI screens; other browsers get a normal image.
|Code=<picture>
  &lt;source
    media="(min-width: 1024px)"
    srcset="opera-fullshot-1x.jpg 1x, opera-fullshot-2x.jpg 2x, opera-fullshot-3x.jpg 3x">
  <img
    src="opera-closeup-1x.jpg" alt="The Oslo Opera House"
   srcset="opera-closeup-2x.jpg 2x, opera-closeup-3x.jpg 3x">
</picture>
}}{{Single Example
|Language=HTML
|Description='''Changing image sizes & art direction use case:''' For browser windows with a width of 1280 CSS pixels and wider, a full-shot photo with a width of 50% of the viewport width is used; for browser windows with a width of 640-1279 CSS pixels, a photo with a width of 60% of the viewport width is used; for less wide browser windows, a photo with a width that is equal to the full viewport width is used. In each case, the browser picks the optional image from a selection of images with widths of 200px, 400px, 800px and 1200px, keeping in mind image width and screen DPI.
|Code=<picture>
  &lt;source
    media="(min-width: 1280px)"
    sizes="50vw"
    srcset="opera-fullshot-200.jpg 200w, opera-fullshot-400.jpg 400w, opera-fullshot-800.jpg 800w, opera-fullshot-1200.jpg 1200w">
  <img
    src="opera-fallback.jpg"
    alt="The Oslo Opera House"
    sizes="(min-width: 640px) 60vw, 100vw"
    srcset="opera-closeup-200.jpg 200w, opera-closeup-400.jpg 400w, opera-closeup-800.jpg 800w, opera-closeup-1200.jpg 1200w">
</picture>
}}
}}
{{Notes_Section
|Usage=The picture element is not a general replacement for the img element. When there is only a single image source, authors should use <code>&lt;img&gt;</code> as usual.

The picture element requires <code>&lt;source&gt;</code> nested as a child.

The picture element requires <code>&lt;img&gt;</code> nested as the last child; without the img element, <code>&lt;picture&gt;</code> will be ignored. This requirement ensures maximum accessibility and browser backwards compatibility.

For accessibility, place alternative text for all images in the <code>alt</code> attribute of the img element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RICG
|URL=http://picture.responsiveimages.org/
|Status=Superseded
}}{{Related Specification
|Name=WHATWG
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/embedded-content.html#embedded-content
|Status=Living Standard
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=* [http://docs.webplatform.org/wiki/html/elements/img &lt;img&gt; Element]
* [http://docs.webplatform.org/wiki/html/elements/source &lt;source&gt; Element]
|External_links=* [http://dev.opera.com/articles/responsive-images/ Responsive Images: Use Cases and Documented Code Snippets to Get You Started]
}}
{{Topics|DOM, HTML, Media}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=DevOpera
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}