{{Page_Title}}
{{Flags
}}
{{Summary_Section|This guide offers a detailed introduction to the main important things to know about SVG.}}
{{Guide
|Content===SVG Primer: Basic shapes and effects==

=== Introduction ===

SVG is a technology that has been on the cusp of greatness for a long time now.  With browser support improving, and three of the big four browser engines already incorporating <a href="http://www.codedread.com/svg-support.php">solid support for SVG</a>, it is an ideal time to start looking into what the technology offers.  This first article will get you comfortable with the basics, so that you are ready to dig deeper and explore SVG further.  Even these baby steps will produce results that can be incorporated straight into your progressively enhanced designs.  The latest W3C candidate recommendation is SVG 1.1, so this is the version I will follow.  SVG Tiny 1.2 is in working draft at the time of writing, and is partially supported by Opera 9.5 and above.

=== SVG overview ===

Since very early on, the web has been primarily made up of text and images, and more recently video and audio have also started to make a regular appearance.  SVG is primarily an image format, but can incorporate all these things.  Unlike image formats you may be more familiar with such as PNG or JPEG (raster image formats), SVG is a vector format.  In this respect it is related to similar technologies such as Adobe Flash and Microsoft Silverlight.  SVG however is an open format, based on XML, which is not controlled by one corporation.  

The big advantage of vector graphic formats over raster formats is that they are maths based instead of pixel based, meaning that rather than having to store information about each individual pixel in the image, mathematical equations are used to calculate their position and other attributes. This means that they are fully scaleable - unlike a raster image, a SVG file will not turn pixelated when zooming in on the image, in a similar fashion to how text doesn't pixelate when you make it larger using the zoom feature of your browser, or increasing the text size.  You can imagine how SVG will benefit the quality of a page design now that zooming is becoming increasingly common due to the take off of the web on alternative devices.  Opera Mini 4 and The Wii Internet Channel are two examples of browsers that make heavy use of zooming.  

This sounds ideal, but remember that not all images are suitable for vector graphics.  While illustrations are a perfect use case for SVG, photographs and (non-cartoon) movies are much better suited to the typical raster formats (eg Bitmap and JPEG.)
 
One key advantage of SVG is that it plays well with other Open Web standards.  You can style it with CSS, add behavior using JavaScript and the DOM, pull in data using XHR, include it within XHTML documents, link to it from HTML and CSS, and so on. This allows you to use knowledge you have already learned, and incorporate it into existing sites.

Another advantage of SVG is that, due to it being based on XML, an image can be created using nothing but a text editor.  This is perfectly reasonable for the basic images we will be creating here, but as images get more complex it is more likely that you’ll want to use an authoring tool – unless you are a super-hero.  Fortunately if your drawing application of choice is Adobe Illustrator, then you are in luck.  You can just export your creation as an SVG file.  Otherwise Inkscape is a good free application that uses SVG as its native format.  You may ask why you should learn SVG if your application of choice supports exporting automatically?  Just like web authoring tools don’t create great HTML and CSS, the same is true of SVG.  Having knowledge of SVG will allow you to optimise those images, and will help a great deal if you want to use scripting to alter or animate SVG files.  It may also be faster to makes changes to a file, or create a simple shape by hand.  

=== Incorporating SVG in your site or application ===

There are a number of ways you can incorporate SVG into your site or application.  You can create a SVG file, with the .svg file extension and just link to it like you would with any other document.  If you would like to incorporate it as an element of an existing page, there are a few options; referencing the URI of the SVG from the <code>img</code> (Opera or WebKit only) or <code>object</code> elements, from CSS via the <code>background-image</code> or <code>list-style-image</code> properties (Opera only), or creating a compound document that mixes SVG with other markup languages such as XHTML and MathML. Using this last method requires that XHTML is used and served as XML.  It will not work with documents served as HTML. The HTML5 Working Group are working to specify how SVG can be using within a HTML document served as text/html.

I can include a SVG image with the <code>img</code> element, as I would with any other image format:

<pre>&lt;img src="my-svg-image.svg" width="200" height="400" alt="A beautiful SVG image" /&gt;</pre>

Similarly, I can include my SVG image as a background in CSS in the same way as I normally would for any other image format:

<pre>div.header { background-image: url("my-svg-image.svg"); }</pre>

The SVG file will scale with the size of the element if it doesn’t specify absolute units; more on that later in the article.

=== Creating a basic skeleton ===

In this section I will walk you through creating a basic SVG template, a process that will be simple for anyone familiar with XML or XHTML. The complete example files for this article can be downloaded here (PROVIDE FILES, INSERT ANCHOR)

# Open up a text editor, create a new file, and on the first line add an XML declaration - this lets the SVG viewer know what version of XML is being used, and the document encoding:

<pre>&lt;?xml version="1.0" encoding="UTF-8"?&gt;</pre>

This is often omitted in XHTML files due to it sending IE6 and below into quirks mode, but as IE6 doesn’t support SVG, this is of no concern to us.

# Below the XML declaration, add the SVG DOCTYPE, as follows: 

<pre> &lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
         "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;</pre>

# To complete the skeleton, the root element has to be specified - just like the root element is html in HTML, in SVG it is svg:

<pre>&lt;svg version="1.1" xmlns="http://www.w3.org/2000/svg"&gt;
&lt;/svg&gt;</pre>

Just like in HTML, the contents of the file are included between the opening and closing tags.

=== A note about document sizes ===

In the example above the image will take up 100% of the available height and width by default.  This will be the full browser window if it is a standalone file; if it is a CSS background image then it will be the size of the element that references it.  If you don't want to go with these defaults, then you can specify your own image dimensions using the svg element's height and width attributes.  A suitable unit should be used with the value, for example:

<pre>&lt;svg version="1.1" width="50%" height="50%" xmlns="http://www.w3.org/2000/svg"&gt;</pre>

=== Creating a simple rectangle ===

One of the most basic shapes in SVG is the humble rectangle.  You’ll most likely use these a lot in SVG, especially when referencing SVG via CSS.  A rectangle (or square) is specified using the <code>rect</code> element.  We’ll step through how to create this shape:

# Open up the SVG template in your text editor of choice and rename it as <q>rectangle.svg</q>. 
# Between the SVG tags add the <code>rect</code> element as follows: &lt;rect /&gt; 
# Now the rectangle has to be placed on the canvas, in the required position.  The co-ordinates of the upper left hand corner of the shape are specified using the <code>x<code> and <code>y</code> attributes:&lt;rect x="0" y="0"/&gt;

The width is specified using the <code>width</code> attribute, and the height is specified with (you guessed it) the <code>height</code> attribute:

<pre>&lt;rect x="0" y="0" height="100%" width="100%"/&gt;</pre>

The rectangle above will be drawn at the top left of the image, and cover the full width and height.  It is possible to use any unit that is available to CSS2.1 (such as mm, cm, px, %, em etc.). If there are no units defined, such as with the x and y attributes above, the initial co-ordinates system is used.  Co-ordinates handily map to 1 pixel per coordinate, but can be remapped using transforms, which I wont get into in this article. Although the rectangle covers the entire image, you will not currently be able to see anything, as the rectangle needs to be styled - no presentational data has yet been defined, eg color, stroke width, etc.  This can be done using CSS (both inline with the style attribute, in a style element or in an external file) or using presentational attributes.  I’ll use CSS throughout the examples, but the choice is up to you.  As SVG is a presentational language it is not a big no-no to apply style directly to the elements instead of using CSS files.  Using external files does however have the same advantages as it does with normal HTML - it can reduce file sizes when the same styles are used regularly, and can ease maintenance and reusability.  

To style the rectangle we can add a reference to the external CSS file before the root element, using the following processing instruction:

<pre>&lt;?xml-stylesheet href="rectangle-style.css" type="text/css"?&gt;</pre>

In the CSS file, SVG specific CSS properties can then be added.  The fill property is similar to background-color, and supports the same colour values as specified in CSS2.1, with the addition of the SVG colour keywords (as also included in the CSS3 colour module).  The stroke property sets the colour of the shape outline, not too unlike border-color, and stroke-width sets the thickness of the outline, similar to border-width.  Additional properties will be explored later.

The following CSS styles the rectangle above to have a 1px black outline (referred to as the stroke, in drawing terminology) and a grey fill:

<pre>rect {
    fill: grey;
    stroke: black;
    stroke-width: 1px;
}</pre>

Try creating a CSS file with the rule above, and add the processing instruction to your SVG file above the SVG element.  The final file should look somewhat like the <a href="file here">SVG rectangle</a> I created earlier. While this doesn’t look like much yet, I’ll cover more useful examples after we’ve worked our way through the basic shapes.

=== Circles and ellipses ===

If you thought creating a rectangle was easy, circles and ellipses are also relatively straight forward.  To draw a circle, create a new file and follow the steps below:

Between the SVG tags, add a <code>circle</code> element:

<pre>&lt;circle /&gt;</pre>

Now we need to place the circle on the canvas.  For circles, we specify the position of the centre point of the circle, using the <code>cx</code> and <code>cy</code> attributes:

<pre>&lt;circle cx="50%" cy="50%" /&gt;</pre>

This will place the circle at the centre of the canvas.

Next, to set the size of the circle, we specify the radius using the <code>r</code> attribute:

<pre>&lt;circle cx="50%" cy="50%" r="20%"/&gt;</pre>

As with the rectangle, we can add style using CSS:

<pre>circle {
    fill; red;
    fill-opacity: 0.9;
}</pre>

An ellipse is specified in the same way as a circle, except with the <code>ellipse</code> element, and two different attributes to specify the radius.  The <code>rx</code> attribute sets the radius of the ellipse on the x-axis and the <code>ry</code> attribute sets the radius on the y-axis. The following example adapts the previous circle example, to make the shape into a ellipse:

<pre>&lt;ellipse cx="50%" cy="50%" rx="20%" ry="15%"/&gt;</pre>


=== Draw some lines ===

Next up are lines.  Lines are created using the <code>line</code> element, and four attributes are used to place the line on the canvas.  the <code>x1</code> and <code>y1</code> attributes are used to specify the start of the line:

<pre>&lt;line x1="10%" y1="50%"/&gt;</pre>

The end point of the line is specified with the corresponding <code>x2</code> and <code>y2</code> attributes:

<pre>&lt;line x1="10%" y1="50%" x2="90%" y2="50%"/&gt;</pre>

You will have noticed if you loaded the SVG file in the browser before specifying the end point of the line that it defaults to the upper left hand corner if a set of co-ordinates are not specified.

As with other shapes, lines have to be styled before it can be seen.  One new property that I’ll introduce is the <code>stroke-linecap</code> property.  This can be used on all other shapes covered so far, and allows the end points of strokes to be styled.  The three possible values are <code>butt</code> (the default), <code>round</code> which adds a rounded cap at the end of the line, and <code>flat</code>, which extends the line by the same value as the stroke width.  In this example, I'll style the line with a rounded line cap:

<pre>line {
	stroke: blue;
 	stroke-width: 2%; 
	stroke-linecap: round;
}</pre>

Make any shape you please with the polygon and polyline elements

With the polygon element you can create more complex  enclosed shapes.  Unlike the previous shapes that I've defined with percentage units, the points in a polygon have to be defined using the co-ordinate system.  As previously mentioned, co-ordinates map one to one with CSS pixels. The co-ordinate model can be adjusted using the <code>viewBox</code> or <code>transform</code> attribute, but this is beyond the scope of this article.  

To draw a triangle (the most basic of polygons), create a new SVG file called triangle.svg and specify a polygon element:

<pre>&lt;polygon points="x,y x,y x,y" /&gt;</pre>

The points attribute defines a space separated list of points. The x and y coordinate must be specified for each point.  The polygon has to be styled like any other shape:

<pre>polygon { 
	Fill: blue;
	Stroke: black;
	Stroke-width: 3;
}</pre>

View the finished triangle example [add e.g.].

I will leave you to experiment with creating more complex shapes, such as the star I have defined below:

[add star example]


View star example [add start eg]

The last shape I want to introduce to you is the polyline.  A polyline is the same as a polygon, except the shape is open instead of closed–meaning that no line will be drawn between the last point and first points.  A polyline is define exactly the same way as a polygon, except using the polyline element:

<pre>&lt;polyline points="x,y x,y x,y" /&gt;</pre>

View polyline example (add example)

All shapes in this article can be defined using the path element, which is the basic building block of SVG.  The basic shapes are included in SVG to make it easier for developers to define common shapes, as path elements are not particularly easy to read or write.  I'll not describe how to use the path element in this article, as it could be an entire article in itself.  Most authoring tools will use the path element to define shapes, so it is useful to be aware that it exists, even if you don't need to fully understand it.  For complex shapes, I usually create them in a image editor and copy/paste the shape into my hand authored SVG file.

=== Create beautiful buttons using shapes, gradients and filters ===

Now that you know how to draw shapes, it is time to put the knowledge to good use, with a more concrete example. I’ll walk you through an example of how to build a button, by adding gradients, shadows and text.

The first step is to create a rectangle that will serve as the base of the button.  As I'm building a stand alone SVG file for the purpose of the article, I specified the units in co-ordinates instead of making it 100% of the canvas.  I also placed the rectangle 10 co-ordinates from the top and left of the canvas, so that it displays away from the browser chrome:

<pre>&lt;rect x="10" y="10" rx="3" ry="3" height="24" width="100"/&gt;</pre>

You may have noticed the <code>rx</code> and <code>ry</code> attributes.  These are similar to the <code>cx</code> and <code>cy</code> attributes used by the <code>circle</code> element, but are used for specifying the radius of the corners.  

To make the button stand out more, I used a gradient instead of a flat colour to fill the rectangle.  I achieved that by adding a <code>defs</code> element as a child of the <code>svg</code> element, then specifying a <code>linearGradient</code> element with-in it.  The <code>defs</code> element is a container element where all the elements are defined that are not immediately rendered. In this case we are defining a gradient that will be used later in the document by the <code>rect</code> element. The code looks like this:

<pre>&lt;defs&gt;
		&lt;linearGradient id="button-gradient" x1="0" x2="0" y1="0" y2="1"&gt;
			&lt;stop offset="0%" stop-color="rgb(171,199,219)"/&gt;
			&lt;stop offset="100%" stop-color="rgb(117,166,200)"/&gt;
		&lt;/linearGradient&gt;
&lt;/defs&gt;</pre>

You don't have to worry about how the gradient works at this early stage in your SVG education.  The main things you need to be aware of is that gradients need a unique ID, and how to change the direction and colour of the gradient.  The example above is a horizontal linear gradient, with the colour changing from top to bottom in a straight line. It is horizontal because the x1 and x2 values are equal, and the y1 and y2 values are different.  If you want to change it to a vertical gradient set x1 and x2 to different values, and y1 and y2 to identical values.  A diagonal gradient can be achieved if both x1 and x2 have different values and y1 and y2 have different values. To change the colour of the gradient you can change the values of the stop-color attributes.  You can have as many stop elements as you wish, and you can change the offset attribute value to specify where the colour starts. 

To reference the gradient I add it as the value of the fill property (or attribute if adding directly to the element instead of via CSS):

<pre>rect {
    		fill: url(#button-gradient);
}</pre> 

I also created a second gradient with a darker colour at the bottom of the gradient, and used it for the stroke:

<pre>rect {
    		fill: url(#button-gradient);
    		stroke-width: 1px;
    		stroke: url(#button-border-gradient);
}</pre>

This gives the button a little bit of depth.  For additional depth I also created a drop shadow, using a SVG filter.  Again, as with the gradient, you don't need to understand exactly how it works at this stage.  

As many drop shadows have the same values, I often just reference the same filter over and over again in different files. You can even reference a filter (and other types of elements in the defs section) in a different file, so it is possible to  define many effects once and reuse them across your entire set of SVG files.

The drop shadow is defined like the following:

<pre>&lt;filter id="drop-shadow" width="140%" height="140%"&gt;
        	&lt;feOffset result="offset" in="SourceAlpha" dx="0" dy="1"/&gt;
        	&lt;feGaussianBlur result="blurred-offset" in="offset" stdDeviation="1"/&gt;
        	&lt;feBlend in="SourceGraphic" in2="blurred-offset" mode="normal"/&gt;
&lt;/filter&gt;</pre>

As with the gradient, a unique ID has to be used, so that it can be referenced. The width and height also has to be bigger than the element that references the filter, so that there is room to apply the offset without it being cut off.  The values that you may want to change are the dx and dy values of the feOffset element.  These set how far along the x and y axis the shadow is offset. Negative values are allowed.  You may also want to change the stdDeviation value of the feGaussianBlur element.  The higher the value, the more blurred the shadow is. The way the filter works is that it takes the alpha channel of the element that references it, offsets the alpha channel by the amount specified, applies a gaussian blur to the result, then blends it with the original element. This is not very obvious to work our yourself, but once it is written it is easy to use.

The filter is applied to the rectangle in a very similar way to the gradients, but using the <code>filter</code> property:

<pre>rect {
    		fill: url(#button-gradient);
    		filter: url(#drop-shadow);
    		stroke-width: 1px;
    		stroke: url(#button-border-gradient);
}</pre>
 
Now the basic button is finished, we need to add some text:

<pre>&lt;text x="60" y="26"&gt;Hello&lt;/text&gt;</pre>

And style it:

<pre>text {
			fill: white;
			fill-opacity: 0.9;
			font-family: "Helvetica Neue", arial, sans-serif;
			font-size: 14px;
			filter: url(#drop-shadow);
			text-anchor:middle;
			pointer-events: none;
		}</pre>

You may have noticed we applied the same drop shadow to the text, and there are two new properties we've not encountered.  The <code>text-anchor</code> property changes the point that the x and y co-ordinates are anchored to. The default is the bottom left of the text, but I've changed it to the middle, so that it is easier to position in the centre of the rectangle, and easier to transform around the centre point if I wish to do so in the future. The pointer-events property was set to none to stop the text from intercepting events.  If I have any events set on the rectangle, such as a click event to active the button, the text is on top of the rectangle and would stop the event from firing if I clicked on top of the text, unless pointer-events is set to none.

The button is almost complete now, but I added a <code>g</code> element around both the rect and text elements for good measure.  This is another container element, and is designed to group related elements.  I gave it an ID of button, and added <code>role="button"</code> to help screen readers understand it is actually a button and not a random piece of text and a rectangle:

<pre>&lt;g id="button" role="button"&gt;
	&lt;rect …/&gt;
	&lt;text …/&gt;
&lt;/g&gt;</pre>

The final step was to add a cursor, to show the user the button can be clicked:

<pre>g#button { cursor: pointer; }</pre>

<a href="http://people.opera.com/dstorey/images/button.svg">View the final button example</a>

While in this example, the button is a box with text, and much of it could be created with CSS 3 properties, you could make a button of any shape or size.  As another simple example, I've created <a href="http://people.opera.com/dstorey/images/circle-button.svg">a round play button with a triangle play icon</a>. I'll not describe in detail how this was created, as it uses almost the same elements as the regular button, and just switches a rectangle for a circle and the text for a polygon.

=== Using your SVG buttons via CSS ===

Instead of creating standalone buttons, you can use the regular HTML button and reference the SVG file using the CSS background-image property.  There are some differences you should take into account however.  You will have to make the SVG file the same size as the HTML button element, so it fits correctly, or set it so that the SVG file fills 100% of the width and height of the HTML element.  You will not need the SVG text as it already exists in the HTML.  For buttons with icons instead of text, the best way is to specify the text in the HTML button, and hide it using generated content as in the example below, or the CSS method of your choice:

<pre>input#play-button {
	content: "" 
}</pre>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}