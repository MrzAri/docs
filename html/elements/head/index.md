---
title: 'head'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://test.w3.org/html/examples/elements/head/head01.html'
compatibility:
  feature: head
  topic: html
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLHeadElement](/dom/HTMLHeadElement)'
readiness: 'In Progress'
summary: 'The head element (&lt;head&gt;) represents a collection of metadata for the document.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/abort
    - dom/events/afterupdate
    - dom/events/beforecopy
    - dom/events/beforeupdate
    - dom/events/cellchange
    - dom/events/change
    - dom/events/dataavailable
    - dom/events/datasetchanged
    - dom/events/datasetcomplete
    - dom/events/error
    - dom/events/errorupdate
    - dom/events/filterchange
    - dom/events/input
    - dom/events/layoutcomplete
    - dom/events/readystatechange
    - dom/events/reset
    - dom/events/resize
    - dom/events/rowenter
    - dom/events/rowexit
    - dom/events/rowsdelete
    - dom/events/rowsinserted
    - dom/events/selectstart
    - dom/methods/appendChild
    - dom/methods/applyElement
    - dom/methods/attachEvent
    - dom/methods/clearAttributes
    - dom/methods/click
    - dom/events/click
    - dom/methods/cloneNode
    - dom/methods/componentFromPoint
    - dom/methods/detachEvent
    - dom/methods/doScroll
    - dom/methods/dragDrop
    - dom/methods/fireEvent
    - dom/methods/getAdjacentText
    - dom/methods/getAttribute
    - dom/methods/getAttributeNode
    - dom/attributes
    - dom/methods/getAttributeNodeNS
    - dom/methods/getAttributeNS
    - dom/methods/getElementsByClassName
    - dom/properties/className
    - dom/methods/getElementsByTagName
    - dom/methods/getElementsByTagNameNS
    - dom/methods/hasAttribute
    - dom/methods/hasAttributeNS
    - dom/methods/hasAttributes
    - dom/methods/hasChildNodes
    - dom/methods/insertAdjacentElement
    - dom/methods/insertAdjacentHTML
    - dom/methods/insertAdjacentText
    - dom/methods/insertBefore
    - dom/methods/mergeAttributes
    - dom/methods/matchesSelector
    - dom/methods/normalize
    - dom/methods/removeAttribute
    - dom/methods/removeAttributeNode
    - dom/methods/removeAttributeNS
    - dom/methods/removeChild
    - dom/methods/removeNode
    - dom/methods/replaceAdjacentText
    - dom/methods/replaceChild
    - dom/methods/replaceNode
    - dom/methods/setActive
    - dom/methods/setAttribute
    - dom/methods/setAttributeNode
    - dom/methods/setAttributeNodeNS
    - dom/methods/setAttributeNS
    - dom/methods/setCapture
    - dom/methods/swapNode
    - dom/properties/attributes
    - dom/properties/canHaveChildren
    - dom/properties/canHavedom/canHaveHTML
    - dom/traversal/properties/childElementCount
    - dom/properties/nodeType
    - dom/properties/constructor
    - dom/properties/firstChild
    - dom/properties/childNodes
    - dom/traversal/properties/firstElementChild
    - dom/properties/innerdom/innerHTML
    - dom/properties/innerText
    - dom/properties/isContentEditable
    - dom/properties/isDisabled
    - dom/properties/isMultiLine
    - dom/traversal/properties/isTextEdit
    - dom/traversal/TextRange
    - dom/properties/lastChild
    - dom/traversal/properties/lastElementChild
    - dom/traversal/properties/nextElementSibling
    - dom/properties/nextSibling
    - dom/properties/nodeName
    - dom/properties/nodeValue
    - dom/properties/offsetHeight
    - dom/properties/offsetParent
    - dom/properties/offsetTop
    - dom/properties/offsetLeft
    - dom/properties/offsetWidth
    - dom/properties/outerdom/outerHTML
    - dom/properties/outerText
    - dom/properties/ownerDocument
    - dom/traversal/properties/parentElement
    - dom/properties/parentNode
    - dom/traversal/properties/parentTextEdit
    - dom/traversal/properties/previousElementSibling
    - dom/properties/previousSibling
    - dom/properties/readyState
    - dom/properties/scrollHeight
    - dom/properties/scrollLeft
    - dom/properties/scrollTop
    - dom/properties/scrollWidth
    - dom/properties/sourceIndex
    - dom/properties/all
    - dom/properties/tagName
    - dom/properties/tagUrn
    - dom/properties/uniqueID
    - dom/properties/uniqueNumber
uri: html/elements/head

---
<p><br/></p>
<h2>Summary</h2>
<p>
The head element (&amp;lt;head&amp;gt;) represents a collection of metadata for the document.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLHeadElement">HTMLHeadElement</a></dd>
</dl><p>The <code>head</code> element provides information that does not affect the rendering of the document but could be of use to the application, such as: title of the document displayed in the tab of the web browser (&lt;title&gt;) and meta information useful for search engines (&lt;meta&gt;).
</p><p>The following tags are valid in this element:
</p>
<ul><li><a href="/html/elements/base"><code>base</code></a></li>
<li><a href="/html/elements/link"><code>link</code></a></li>
<li><a href="/html/elements/meta"><code>meta</code></a></li>
<li><a href="/html/elements/script"><code>script</code></a></li>
<li><a href="/html/elements/style"><code>style</code></a></li>
<li><a href="/html/elements/title"><code>title</code></a></li></ul><h2>Examples</h2>
<p>The <code>&lt;head&gt;</code> element is contained by the <code>&lt;html&gt;</code> element and contains the <code>&lt;title&gt;</code> element.
</p>
<div class="example">
<pre class="html">

<pre class="html">
&lt;!doctype html&gt;
&lt;html lang="en"&gt;
&lt;head&gt;
&lt;meta charset="utf-8"&gt;
&lt;title&gt;The HTML Document&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;The HTML content&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</pre>
<p><a rel="nofollow" class="external text" href="http://test.w3.org/html/examples/elements/head/head01.html">View live example</a>
</p>
</div>
<p><br/></p>
<h3>Members</h3>
<p>The <code>head</code> object has these types of members:
</p>
<ul><li><a href="#Events">Events</a></li>
<li><a href="#Methods">Methods</a></li>
<li><a href="#Properties">Properties</a></li></ul><p><br/></p>
<h4>Events</h4>
<p>The <code>head</code> object has these events.
</p>
<table class="wikitable"><tr><th>Event
</th>
<th>Description
</th></tr><tr><td><a href="/w/index.php?title=dom/events/abort&amp;action=edit&amp;redlink=1" class="new"><code>onabort</code></a>
</td>
<td>Fires when the user aborts the download.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/afterupdate&amp;action=edit&amp;redlink=1" class="new"><code>onafterupdate</code></a>
</td>
<td>Fires on a databound object after successfully updating the associated data in the data source object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/beforecopy&amp;action=edit&amp;redlink=1" class="new"><code>onbeforecopy</code></a>
</td>
<td>Fires on the source object before the selection is copied to the system clipboard.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/beforeupdate&amp;action=edit&amp;redlink=1" class="new"><code>onbeforeupdate</code></a>
</td>
<td>Fires on a databound object before updating the associated data in the data source object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/cellchange&amp;action=edit&amp;redlink=1" class="new"><code>oncellchange</code></a>
</td>
<td>Fires when data changes in the data provider.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/change&amp;action=edit&amp;redlink=1" class="new"><code>onchange</code></a>
</td>
<td>Fires when the contents of the object or selection have changed.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/dataavailable&amp;action=edit&amp;redlink=1" class="new"><code>ondataavailable</code></a>
</td>
<td>Fires periodically as data arrives from data source objects that asynchronously transmit their data.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/datasetchanged&amp;action=edit&amp;redlink=1" class="new"><code>ondatasetchanged</code></a>
</td>
<td>Fires when the data set exposed by a data source object changes.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/datasetcomplete&amp;action=edit&amp;redlink=1" class="new"><code>ondatasetcomplete</code></a>
</td>
<td>Fires to indicate that all data is available from the data source object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/error&amp;action=edit&amp;redlink=1" class="new"><code>onerror</code></a>
</td>
<td>Fires when an error occurs during object loading.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/errorupdate&amp;action=edit&amp;redlink=1" class="new"><code>onerrorupdate</code></a>
</td>
<td>Fires on a databound object when an error occurs while updating the associated data in the data source object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/filterchange&amp;action=edit&amp;redlink=1" class="new"><code>onfilterchange</code></a>
</td>
<td>Fires when a visual filter changes state or completes a transition.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/input&amp;action=edit&amp;redlink=1" class="new"><code>oninput</code></a>
</td>
<td>Occurs when the text content of an element is changed through the user interface.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/layoutcomplete&amp;action=edit&amp;redlink=1" class="new"><code>onlayoutcomplete</code></a>
</td>
<td>Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
</td></tr><tr><td><a href="/dom/events/load" class="mw-redirect"><code>onload</code></a>
</td>
<td>Fires immediately after the client loads the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/readystatechange&amp;action=edit&amp;redlink=1" class="new"><code>onreadystatechange</code></a>
</td>
<td>Fires when the state of the object has changed.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/reset&amp;action=edit&amp;redlink=1" class="new"><code>onreset</code></a>
</td>
<td>Fires when the user resets a form.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/resize&amp;action=edit&amp;redlink=1" class="new"><code>onresize</code></a>
</td>
<td>Fires when the size of the object is about to change.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/rowenter&amp;action=edit&amp;redlink=1" class="new"><code>onrowenter</code></a>
</td>
<td>Fires to indicate that the current row has changed in the data source and new data values are available on the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/rowexit&amp;action=edit&amp;redlink=1" class="new"><code>onrowexit</code></a>
</td>
<td>Fires just before the data source control changes the current row in the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/rowsdelete&amp;action=edit&amp;redlink=1" class="new"><code>onrowsdelete</code></a>
</td>
<td>Fires when rows are about to be deleted from the recordset.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/rowsinserted&amp;action=edit&amp;redlink=1" class="new"><code>onrowsinserted</code></a>
</td>
<td>Fires just after new rows are inserted in the current recordset.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/selectstart&amp;action=edit&amp;redlink=1" class="new"><code>onselect</code></a>
</td>
<td>Fires when the current selection changes.
</td></tr></table><p> 
</p>
<h4>Methods</h4>
<p>The <code>head</code> object has these methods.
</p>
<table class="wikitable"><tr><th>Method
</th>
<th>Description
</th></tr><tr><td><code>addBehavior</code>
</td>
<td>Attaches a behavior to the element.
<p>This method is not supported for Metro style apps using JavaScript.
</p>
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/appendChild&amp;action=edit&amp;redlink=1" class="new"><code>appendChild</code></a>
</td>
<td>Appends an element as a child to the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/applyElement&amp;action=edit&amp;redlink=1" class="new"><code>applyElement</code></a>
</td>
<td>Makes the element either a child or parent of another element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/attachEvent&amp;action=edit&amp;redlink=1" class="new"><code>attachEvent</code></a>
</td>
<td>Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/clearAttributes&amp;action=edit&amp;redlink=1" class="new"><code>clearAttributes</code></a>
</td>
<td>Removes all attributes and values from the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/click&amp;action=edit&amp;redlink=1" class="new"><code>click</code></a>
</td>
<td>Simulates a click by causing the <a href="/w/index.php?title=dom/events/click&amp;action=edit&amp;redlink=1" class="new"><code>onclick</code></a> event to fire.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/cloneNode&amp;action=edit&amp;redlink=1" class="new"><code>cloneNode</code></a>
</td>
<td>Copies a reference to the object from the document hierarchy.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/componentFromPoint&amp;action=edit&amp;redlink=1" class="new"><code>componentFromPoint</code></a>
</td>
<td>Returns the component located at the specified coordinates via certain events.
</td></tr><tr><td><code>contains</code>
</td>
<td>Checks whether the given element is contained within the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/detachEvent&amp;action=edit&amp;redlink=1" class="new"><code>detachEvent</code></a>
</td>
<td>Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/doScroll&amp;action=edit&amp;redlink=1" class="new"><code>doScroll</code></a>
</td>
<td>Simulates a click on a scroll bar component.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/dragDrop&amp;action=edit&amp;redlink=1" class="new"><code>dragDrop</code></a>
</td>
<td>Initiates a drag event.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/fireEvent&amp;action=edit&amp;redlink=1" class="new"><code>fireEvent</code></a>
</td>
<td>Fires a specified event on the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAdjacentText&amp;action=edit&amp;redlink=1" class="new"><code>getAdjacentText</code></a>
</td>
<td>Returns the adjacent text string.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttribute&amp;action=edit&amp;redlink=1" class="new"><code>getAttribute</code></a>
</td>
<td>Retrieves the value of the specified attribute.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttributeNode&amp;action=edit&amp;redlink=1" class="new"><code>getAttributeNode</code></a>
</td>
<td>Retrieves an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attribute</code></a> object referenced by the <code>attribute&lt;code&gt;.<a href="/html/attributes/name">&lt;code&gt;name</a></code> property.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttributeNodeNS&amp;action=edit&amp;redlink=1" class="new"><code>getAttributeNodeNS</code></a>
</td>
<td>Gets an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attribute</code></a> object that matches the specified namespace and name.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttributeNS&amp;action=edit&amp;redlink=1" class="new"><code>getAttributeNS</code></a>
</td>
<td>Gets the value of the specified attribute within the specified namespace.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getElementsByClassName&amp;action=edit&amp;redlink=1" class="new"><code>getElementsByClassName</code></a>
</td>
<td>Gets a collection of objects that are based on the value of the <a href="/w/index.php?title=dom/properties/className&amp;action=edit&amp;redlink=1" class="new"><code>CLASS</code></a> attribute.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getElementsByTagName&amp;action=edit&amp;redlink=1" class="new"><code>getElementsByTagName</code></a>
</td>
<td>Retrieves a collection of objects based on the specified element name.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getElementsByTagNameNS&amp;action=edit&amp;redlink=1" class="new"><code>getElementsByTagNameNS</code></a>
</td>
<td>Gets a collection of objects that are based on the specified element names within a specified namespace.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/hasAttribute&amp;action=edit&amp;redlink=1" class="new"><code>hasAttribute</code></a>
</td>
<td>Determines whether an attribute with the specified name exists.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/hasAttributeNS&amp;action=edit&amp;redlink=1" class="new"><code>hasAttributeNS</code></a>
</td>
<td>Determines whether an attribute that has the specified namespace and name exists.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/hasAttributes&amp;action=edit&amp;redlink=1" class="new"><code>hasAttributes</code></a>
</td>
<td>Determines whether one or more attributes exist for the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/hasChildNodes&amp;action=edit&amp;redlink=1" class="new"><code>hasChildNodes</code></a>
</td>
<td>Returns a value that indicates whether the object has children.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/insertAdjacentElement&amp;action=edit&amp;redlink=1" class="new"><code>insertAdjacentElement</code></a>
</td>
<td>Inserts an element at the specified location.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/insertAdjacentHTML&amp;action=edit&amp;redlink=1" class="new"><code>insertAdjacentHTML</code></a>
</td>
<td>Inserts the given HTML text into the element at the location.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/insertAdjacentText&amp;action=edit&amp;redlink=1" class="new"><code>insertAdjacentText</code></a>
</td>
<td>Inserts the given text into the element at the specified location.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/insertBefore&amp;action=edit&amp;redlink=1" class="new"><code>insertBefore</code></a>
</td>
<td>Inserts an element into the document hierarchy as a child node of a parent object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/mergeAttributes&amp;action=edit&amp;redlink=1" class="new"><code>mergeAttributes</code></a>
</td>
<td>Copies all read/write attributes to the specified element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/matchesSelector&amp;action=edit&amp;redlink=1" class="new"><code>msMatchesSelector</code></a>
</td>
<td>Determines whether an object matches the specified selector.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/normalize&amp;action=edit&amp;redlink=1" class="new"><code>normalize</code></a>
</td>
<td>Merges adjacent DOM objects to produce a normalized document object model.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeAttribute&amp;action=edit&amp;redlink=1" class="new"><code>removeAttribute</code></a>
</td>
<td>Removes an attribute from an object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeAttributeNode&amp;action=edit&amp;redlink=1" class="new"><code>removeAttributeNode</code></a>
</td>
<td>Removes an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attribute</code></a> object from the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeAttributeNS&amp;action=edit&amp;redlink=1" class="new"><code>removeAttributeNS</code></a>
</td>
<td>Removes the specified attribute from the object.
</td></tr><tr><td><code>removeBehavior</code>
</td>
<td>Detaches a behavior from the element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeChild&amp;action=edit&amp;redlink=1" class="new"><code>removeChild</code></a>
</td>
<td>Removes a child node from the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeNode&amp;action=edit&amp;redlink=1" class="new"><code>removeNode</code></a>
</td>
<td>Removes the object from the document hierarchy.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/replaceAdjacentText&amp;action=edit&amp;redlink=1" class="new"><code>replaceAdjacentText</code></a>
</td>
<td>Replaces the text adjacent to the element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/replaceChild&amp;action=edit&amp;redlink=1" class="new"><code>replaceChild</code></a>
</td>
<td>Replaces an existing child element with a new child element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/replaceNode&amp;action=edit&amp;redlink=1" class="new"><code>replaceNode</code></a>
</td>
<td>Replaces the object with another element.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setActive&amp;action=edit&amp;redlink=1" class="new"><code>setActive</code></a>
</td>
<td>Sets the object as active without setting focus to the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttribute&amp;action=edit&amp;redlink=1" class="new"><code>setAttribute</code></a>
</td>
<td>Sets the value of the specified attribute.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttributeNode&amp;action=edit&amp;redlink=1" class="new"><code>setAttributeNode</code></a>
</td>
<td>Sets an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attribute</code></a> object node as part of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttributeNodeNS&amp;action=edit&amp;redlink=1" class="new"><code>setAttributeNodeNS</code></a>
</td>
<td>Sets an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attribute</code></a> object as part of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttributeNS&amp;action=edit&amp;redlink=1" class="new"><code>setAttributeNS</code></a>
</td>
<td>Sets the value of the specified attribute within the specified namespace.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setCapture&amp;action=edit&amp;redlink=1" class="new"><code>setCapture</code></a>
</td>
<td>Sets the mouse capture to the object that belongs to the current document.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/swapNode&amp;action=edit&amp;redlink=1" class="new"><code>swapNode</code></a>
</td>
<td>Exchanges the location of two objects in the document hierarchy.
</td></tr></table><p> 
</p>
<h4>Properties</h4>
<p>The <code>head</code> object has these properties.
</p>
<table class="wikitable"><tr><th>Property
</th>
<th>Description
</th></tr><tr><td><a href="/w/index.php?title=dom/properties/attributes&amp;action=edit&amp;redlink=1" class="new"><code>attributes</code></a>
</td>
<td>Retrieves a collection of attributes of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/canHaveChildren&amp;action=edit&amp;redlink=1" class="new"><code>canHaveChildren</code></a>
</td>
<td>Gets a value indicating whether the object can contain child objects.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/canHavedom/canHaveHTML&amp;action=edit&amp;redlink=1" class="new"><code>canHaveHTML</code></a>
</td>
<td>Retrieves the value indicating whether the object can contain rich HTML markup.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/childElementCount&amp;action=edit&amp;redlink=1" class="new"><code>childElementCount</code></a>
</td>
<td>Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. <a href="/w/index.php?title=dom/traversal/properties/childElementCount&amp;action=edit&amp;redlink=1" class="new"><code>childElementCount</code></a> does not return all child nodes, only child nodes that are <a href="/w/index.php?title=dom/properties/nodeType&amp;action=edit&amp;redlink=1" class="new"><code>nodeType</code></a> =1, or element nodes.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/className&amp;action=edit&amp;redlink=1" class="new"><code>className</code></a>
</td>
<td>Sets or retrieves the class of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/constructor&amp;action=edit&amp;redlink=1" class="new"><code>constructor</code></a>
</td>
<td>Returns a reference to the constructor of an object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/firstChild&amp;action=edit&amp;redlink=1" class="new"><code>firstChild</code></a>
</td>
<td>Gets a reference to the first child in the <a href="/w/index.php?title=dom/properties/childNodes&amp;action=edit&amp;redlink=1" class="new"><code>childNodes</code></a> collection of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/firstElementChild&amp;action=edit&amp;redlink=1" class="new"><code>firstElementChild</code></a>
</td>
<td>Retrieves a reference to the first child element, or null if there are no child elements.
</td></tr><tr><td><a href="/html/attributes/id"><code>id</code></a>
</td>
<td>Sets or retrieves the string identifying the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/innerdom/innerHTML&amp;action=edit&amp;redlink=1" class="new"><code>innerHTML</code></a>
</td>
<td>Sets or retrieves the HTML between the start and end tags of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/innerText&amp;action=edit&amp;redlink=1" class="new"><code>innerText</code></a>
</td>
<td>Sets or retrieves the text between the start and end tags of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/isContentEditable&amp;action=edit&amp;redlink=1" class="new"><code>isContentEditable</code></a>
</td>
<td>Gets the value that indicates whether the user can edit the contents of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/isDisabled&amp;action=edit&amp;redlink=1" class="new"><code>isDisabled</code></a>
</td>
<td>Gets the value that indicates whether the user can interact with the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/isMultiLine&amp;action=edit&amp;redlink=1" class="new"><code>isMultiLine</code></a>
</td>
<td>Retrieves the value indicating whether the content of the object contains one or more lines.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/isTextEdit&amp;action=edit&amp;redlink=1" class="new"><code>isTextEdit</code></a>
</td>
<td>Retrieves whether a <a href="/w/index.php?title=dom/traversal/TextRange&amp;action=edit&amp;redlink=1" class="new"><code>TextRange</code></a> object can be created using the object.
</td></tr><tr><td><a href="/html/attributes/lang"><code>lang</code></a>
</td>
<td>Sets or retrieves the language to use.
</td></tr><tr><td><a href="/html/attributes/language"><code>language</code></a>
</td>
<td>Sets or retrieves the language in which the current script is written.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/lastChild&amp;action=edit&amp;redlink=1" class="new"><code>lastChild</code></a>
</td>
<td>Gets a reference to the last child in the <a href="/w/index.php?title=dom/properties/childNodes&amp;action=edit&amp;redlink=1" class="new"><code>childNodes</code></a> collection of an object.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/lastElementChild&amp;action=edit&amp;redlink=1" class="new"><code>lastElementChild</code></a>
</td>
<td>Retrieves a reference to the last child element or null if there are no child elements.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/nextElementSibling&amp;action=edit&amp;redlink=1" class="new"><code>nextElementSibling</code></a>
</td>
<td>Retrieves a reference to the sibling element that immediately follows or null if the element does not have any sibling elements that follow it.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/nextSibling&amp;action=edit&amp;redlink=1" class="new"><code>nextSibling</code></a>
</td>
<td>Retrieves a reference to the next child of the parent for the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/nodeName&amp;action=edit&amp;redlink=1" class="new"><code>nodeName</code></a>
</td>
<td>Gets the name of a particular type of node.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/nodeType&amp;action=edit&amp;redlink=1" class="new"><code>nodeType</code></a>
</td>
<td>Retrieves the type of the requested node.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/nodeValue&amp;action=edit&amp;redlink=1" class="new"><code>nodeValue</code></a>
</td>
<td>Gets or sets the value of a node.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/offsetHeight&amp;action=edit&amp;redlink=1" class="new"><code>offsetHeight</code></a>
</td>
<td>Retrieves the height of the object relative to the layout or coordinate parent, as specified by the <a href="/w/index.php?title=dom/properties/offsetParent&amp;action=edit&amp;redlink=1" class="new"><code>offsetParent</code></a> property.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/offsetParent&amp;action=edit&amp;redlink=1" class="new"><code>offsetParent</code></a>
</td>
<td>Retrieves a reference to the container object that defines the <a href="/w/index.php?title=dom/properties/offsetTop&amp;action=edit&amp;redlink=1" class="new"><code>offsetTop</code></a> and <a href="/w/index.php?title=dom/properties/offsetLeft&amp;action=edit&amp;redlink=1" class="new"><code>offsetLeft</code></a> properties of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/offsetWidth&amp;action=edit&amp;redlink=1" class="new"><code>offsetWidth</code></a>
</td>
<td>Retrieves the width of the object relative to the layout or coordinate parent, as specified by the <a href="/w/index.php?title=dom/properties/offsetParent&amp;action=edit&amp;redlink=1" class="new"><code>offsetParent</code></a> property.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/outerdom/outerHTML&amp;action=edit&amp;redlink=1" class="new"><code>outerHTML</code></a>
</td>
<td>Sets or retrieves the object and its content in HTML.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/outerText&amp;action=edit&amp;redlink=1" class="new"><code>outerText</code></a>
</td>
<td>Sets or retrieves the text of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/ownerDocument&amp;action=edit&amp;redlink=1" class="new"><code>ownerDocument</code></a>
</td>
<td>Retrieves the <a href="/dom/Document"><code>Document</code></a> object associated with the node.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/parentElement&amp;action=edit&amp;redlink=1" class="new"><code>parentElement</code></a>
</td>
<td>Retrieves the parent object in the object hierarchy.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/parentNode&amp;action=edit&amp;redlink=1" class="new"><code>parentNode</code></a>
</td>
<td>Retrieves the parent object in the document hierarchy.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/parentTextEdit&amp;action=edit&amp;redlink=1" class="new"><code>parentTextEdit</code></a>
</td>
<td>Retrieves the container object in the document hierarchy that can be used to create a <a href="/w/index.php?title=dom/traversal/TextRange&amp;action=edit&amp;redlink=1" class="new"><code>TextRange</code></a> containing the original object.
</td></tr><tr><td><a href="/w/index.php?title=dom/traversal/properties/previousElementSibling&amp;action=edit&amp;redlink=1" class="new"><code>previousElementSibling</code></a>
</td>
<td>Retrieves a reference to the immediately preceding sibling element or null if the element does not have any preceding siblings.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/previousSibling&amp;action=edit&amp;redlink=1" class="new"><code>previousSibling</code></a>
</td>
<td>Gets a reference to the previous child of the parent for the object.
</td></tr><tr><td><code>profile</code>
</td>
<td>Sets or retrieves  one or more URIs in which the object properties and legal values for those properties are defined.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/readyState&amp;action=edit&amp;redlink=1" class="new"><code>readyState</code></a>
</td>
<td>Retrieves the current state of the object.
</td></tr><tr><td><code>recordNumber</code>
</td>
<td>Retrieves the ordinal record from the data set that generated the object.
</td></tr><tr><td><a href="/html/attributes/role"><code>role</code></a>
</td>
<td>Sets or retrieves the role for this element.
</td></tr><tr><td><code>scopeName</code>
</td>
<td>Gets the namespace defined for the element.
<p>This property is not supported for Metro style apps using JavaScript.
</p>
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/scrollHeight&amp;action=edit&amp;redlink=1" class="new"><code>scrollHeight</code></a>
</td>
<td>Retrieves the scrolling height of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/scrollLeft&amp;action=edit&amp;redlink=1" class="new"><code>scrollLeft</code></a>
</td>
<td>Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/scrollTop&amp;action=edit&amp;redlink=1" class="new"><code>scrollTop</code></a>
</td>
<td>Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/scrollWidth&amp;action=edit&amp;redlink=1" class="new"><code>scrollWidth</code></a>
</td>
<td>Retrieves the scrolling width of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/sourceIndex&amp;action=edit&amp;redlink=1" class="new"><code>sourceIndex</code></a>
</td>
<td>Retrieves the ordinal position of the object, in source order, as the object appears in the document's <a href="/w/index.php?title=dom/properties/all&amp;action=edit&amp;redlink=1" class="new"><code>all</code></a> collection.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/tagName&amp;action=edit&amp;redlink=1" class="new"><code>tagName</code></a>
</td>
<td>Retrieves the tag name of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/tagUrn&amp;action=edit&amp;redlink=1" class="new"><code>tagUrn</code></a>
</td>
<td>Sets or gets the URN specified in the namespace declaration.
<p>This property is not supported for Metro style apps using JavaScript.
</p>
</td></tr><tr><td><a href="/html/attributes/title"><code>title</code></a>
</td>
<td>Sets or retrieves advisory information (a ToolTip) for the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/uniqueID&amp;action=edit&amp;redlink=1" class="new"><code>uniqueID</code></a>
</td>
<td>Retrieves an autogenerated, unique identifier for the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/uniqueNumber&amp;action=edit&amp;redlink=1" class="new"><code>uniqueNumber</code></a>
</td>
<td>Retrieves the element's unique number.
</td></tr></table><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/document-metadata.html#the-head-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/document-metadata.html#the-head-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/global.html#edef-HEAD">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl><h2>See also</h2>
<h3>Related articles</h3>
<h4>Document Structure</h4>
<ul><li> <a href="/html/elements/button">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button/ja">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/footer">footer</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">head</strong></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/main">main</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/nav">nav</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/p">p</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/section">section</a></li></ul><h4>HTML</h4>
<ul><li> <a href="/css/properties/user-modify">user-modify</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/textLength">textLength</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/value">value</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/accept">accept</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/action">action</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/alt">alt</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autocomplete">autocomplete</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autofocus">autofocus</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/checked">checked</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/crossorigin">crossorigin</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/form">form</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/formEnctype">formEnctype</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/list">list</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/max_(HTMLInputElement)">max (HTMLInputElement)</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/maxLength">maxLength</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/min">min</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/multiple">multiple</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/readonly">readonly</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/size">size</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/standby">standby</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/step">step</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements">HTML Elements</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE/ja">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/acronym">acronym</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b/ja">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br/ja">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button/ja">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/caption">caption</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/cite">cite</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/code">code</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/col">col</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/colgroup">colgroup</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/datalist">datalist</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/del">del</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/dfn">dfn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/div">div</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/em">em</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/embed">EMBED</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/fieldset">fieldset</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/font">font</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/footer">footer</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">head</strong></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hn">hn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hr">hr</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/html">html</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/i">i</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/img">img</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/input">input</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/ins">ins</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/kbd">kbd</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/legend">legend</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/mark">mark</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/option">option</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/p">p</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/samp">samp</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/script">script</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/span">span</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/strong">strong</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/table">table</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tbody">tbody</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/td">td</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tfoot">tfoot</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/th">th</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/time">time</a></li></ul>
