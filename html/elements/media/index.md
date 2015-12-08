---
title: 'media'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: media
  topic: html
notes:
  - 'Deletion Candidate'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
summary: 'Presents audio or video data to the user. The media element provides the audio and video objects which are used to play sound and video content.'
tags:
  - Markup_Elements
  - HTML
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/abort
    - dom/events/blur
    - dom/events/change
    - dom/events/drag
    - dom/events/dragend
    - dom/events/dragenter
    - dom/events/dragleave
    - dom/events/dragover
    - dom/events/drop
    - dom/events/error
    - dom/events/focus
    - dom/events/input
    - dom/events/reset
    - dom/events/scroll
    - dom/events/selectstart
    - apis/audio-video/methods/canPlayType
    - dom/methods/compareDocumentPosition
    - dom/methods/getAttributeNodeNS
    - dom/attributes
    - dom/methods/getAttributeNS
    - dom/methods/getElementsByClassName
    - dom/properties/className
    - dom/methods/getElementsByTagNameNS
    - dom/methods/hasAttributeNS
    - dom/methods/isDefaultNamespace
    - dom/methods/isEqualNode
    - dom/methods/isSameNode
    - dom/methods/isSupported
    - apis/audio-video/methods/load
    - dom/methods/lookupNamespaceURI
    - dom/methods/lookupPrefix
    - dom/methods/matchesSelector
    - apis/audio-video/methods/pause
    - apis/audio-video/properties/paused
    - apis/audio-video/methods/play
    - dom/methods/removeAttributeNS
    - dom/methods/setAttributeNodeNS
    - dom/methods/setAttributeNS
    - apis/audio-video/properties/audioTracks
    - apis/audio-video/properties/autobuffer
    - apis/audio-video/properties/preload
    - apis/audio-video/properties/autoplay
    - apis/audio-video/properties/buffered
    - apis/audio-video/properties/controls
    - apis/audio-video/properties/currentSrc
    - apis/audio-video/properties/currentTime
    - apis/audio-video/properties/defaultPlaybackRate
    - apis/audio-video/properties/duration
    - apis/audio-video/properties/ended
    - apis/audio-video/properties/error
    - apis/audio-video/properties/initialTime
    - dom/properties/localName
    - apis/audio-video/properties/loop
    - apis/audio-video/properties/muted
    - dom/properties/namespaceURI
    - apis/audio-video/properties/networkState
    - apis/audio-video/properties/playbackRate
    - apis/audio-video/properties/played
    - apis/audio-video/HTMLTimeRanges
    - dom/properties/prefix
    - apis/audio-video/properties/seekable
    - apis/audio-video/properties/seeking
    - apis/audio-video/properties/src
    - dom/properties/textContent
    - apis/audio-video/properties/volume
uri: html/elements/media

---
<p><br/></p>
<h2>Summary</h2>
<p>
Presents audio or video data to the user. The media element provides the audio and video objects which are used to play sound and video content.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLElement">HTMLElement</a></dd>
</dl><p><br/></p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=221374">HTML5 A vocabulary and associated APIs for HTML and XHTML</a>, Section 4.8.10</li></ul><p><br/></p>
<h3>Members</h3>
<p>The <b>media</b> object has these types of members:
</p>
<ul><li>[#events Events]</li>
<li>[#methods Methods]</li>
<li>[#properties Properties]</li></ul><p><br/></p>
<h4>Events</h4>
<p>The <b>media</b> object has these events.
</p>
<table class="wikitable"><tr><th>Event
</th>
<th>Description
</th></tr><tr><td><a href="/w/index.php?title=dom/events/abort&amp;action=edit&amp;redlink=1" class="new"><b>onabort</b></a>
</td>
<td>Fires when the user aborts the download.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/blur&amp;action=edit&amp;redlink=1" class="new"><b>onblur</b></a>
</td>
<td>Fires when the object loses the input focus.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/change&amp;action=edit&amp;redlink=1" class="new"><b>onchange</b></a>
</td>
<td>Fires when the contents of the object or selection have changed.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/drag&amp;action=edit&amp;redlink=1" class="new"><b>ondrag</b></a>
</td>
<td>Fires on the source object continuously during a drag operation.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/dragend&amp;action=edit&amp;redlink=1" class="new"><b>ondragend</b></a>
</td>
<td>Fires on the source object when the user releases the mouse at the close of a drag operation.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/dragenter&amp;action=edit&amp;redlink=1" class="new"><b>ondragenter</b></a>
</td>
<td>Fires on the target element when the user drags the object to a valid drop target.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/dragleave&amp;action=edit&amp;redlink=1" class="new"><b>ondragleave</b></a>
</td>
<td>Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/dragover&amp;action=edit&amp;redlink=1" class="new"><b>ondragover</b></a>
</td>
<td>Fires on the target element continuously while the user drags the object over a valid drop target.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/drop&amp;action=edit&amp;redlink=1" class="new"><b>ondrop</b></a>
</td>
<td>Fires on the target object when the mouse button is released during a drag-and-drop operation.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/error&amp;action=edit&amp;redlink=1" class="new"><b>onerror</b></a>
</td>
<td>Fires when an error occurs during object loading.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/focus&amp;action=edit&amp;redlink=1" class="new"><b>onfocus</b></a>
</td>
<td>Fires when the object receives focus.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/input&amp;action=edit&amp;redlink=1" class="new"><b>oninput</b></a>
</td>
<td>Occurs when the text content of an element is changed through the user interface.
</td></tr><tr><td><a href="/dom/events/load" class="mw-redirect"><b>onload</b></a>
</td>
<td>Fires immediately after the client loads the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/reset&amp;action=edit&amp;redlink=1" class="new"><b>onreset</b></a>
</td>
<td>Fires when the user resets a form.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/scroll&amp;action=edit&amp;redlink=1" class="new"><b>onscroll</b></a>
</td>
<td>Fires when the user repositions the scroll box in the scroll bar on the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/events/selectstart&amp;action=edit&amp;redlink=1" class="new"><b>onselect</b></a>
</td>
<td>Fires when the current selection changes.
</td></tr></table><p> 
</p>
<h4>Methods</h4>
<p>The <b>media</b> object has these methods.
</p>
<table class="wikitable"><tr><th>Method
</th>
<th>Description
</th></tr><tr><td><a href="/w/index.php?title=apis/audio-video/methods/canPlayType&amp;action=edit&amp;redlink=1" class="new"><b>canPlayType</b></a>
</td>
<td>Returns a string that specifies whether the client can play a given media resource type.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/compareDocumentPosition&amp;action=edit&amp;redlink=1" class="new"><b>compareDocumentPosition</b></a>
</td>
<td>Compares the position of two nodes in a document.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttributeNodeNS&amp;action=edit&amp;redlink=1" class="new"><b>getAttributeNodeNS</b></a>
</td>
<td>Gets an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><b>attribute</b></a> object that matches the specified namespace and name.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getAttributeNS&amp;action=edit&amp;redlink=1" class="new"><b>getAttributeNS</b></a>
</td>
<td>Gets the value of the specified attribute within the specified namespace.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getElementsByClassName&amp;action=edit&amp;redlink=1" class="new"><b>getElementsByClassName</b></a>
</td>
<td>Gets a collection of objects that are based on the value of the <a href="/w/index.php?title=dom/properties/className&amp;action=edit&amp;redlink=1" class="new"><b>CLASS</b></a> attribute.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/getElementsByTagNameNS&amp;action=edit&amp;redlink=1" class="new"><b>getElementsByTagNameNS</b></a>
</td>
<td>Gets a collection of objects that are based on the specified element names within a specified namespace.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/hasAttributeNS&amp;action=edit&amp;redlink=1" class="new"><b>hasAttributeNS</b></a>
</td>
<td>Determines whether an attribute that has the specified namespace and name exists.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/isDefaultNamespace&amp;action=edit&amp;redlink=1" class="new"><b>isDefaultNamespace</b></a>
</td>
<td>Indicates whether or not a namespace is the default namespace for a document.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/isEqualNode&amp;action=edit&amp;redlink=1" class="new"><b>isEqualNode</b></a>
</td>
<td>Determines if two nodes are equal.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/isSameNode&amp;action=edit&amp;redlink=1" class="new"><b>isSameNode</b></a>
</td>
<td>Determines if two node references refer to the same node.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/isSupported&amp;action=edit&amp;redlink=1" class="new"><b>isSupported</b></a>
</td>
<td>Returns a value indicating whether or not the object supports a specific DOM standard.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/methods/load&amp;action=edit&amp;redlink=1" class="new"><b>load</b></a>
</td>
<td>Resets the <b>IHTMLMediaElement</b> and loads a new media resource.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/lookupNamespaceURI&amp;action=edit&amp;redlink=1" class="new"><b>lookupNamespaceURI</b></a>
</td>
<td>Gets the URI of the namespace associated with a namespace prefix, if any.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/lookupPrefix&amp;action=edit&amp;redlink=1" class="new"><b>lookupPrefix</b></a>
</td>
<td>Gets the namespace prefix associated with a URI, if any.
</td></tr><tr><td><b>msClearEffects</b>
</td>
<td>Clears all effects from the media pipeline.
</td></tr><tr><td><b>msInsertAudioEffect</b>
</td>
<td>Inserts the specified audio effect into media pipeline.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/matchesSelector&amp;action=edit&amp;redlink=1" class="new"><b>msMatchesSelector</b></a>
</td>
<td>Determines whether an object matches the specified selector.
</td></tr><tr><td><b>msSetMediaProtectionManager</b>
</td>
<td>Specifies the media protection manager for a given media pipeline.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/methods/pause&amp;action=edit&amp;redlink=1" class="new"><b>pause</b></a>
</td>
<td>Pauses the current playback and sets <a href="/w/index.php?title=apis/audio-video/properties/paused&amp;action=edit&amp;redlink=1" class="new"><b>paused</b></a> to TRUE.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/methods/play&amp;action=edit&amp;redlink=1" class="new"><b>play</b></a>
</td>
<td>Loads and starts playback of a media resource.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/removeAttributeNS&amp;action=edit&amp;redlink=1" class="new"><b>removeAttributeNS</b></a>
</td>
<td>Removes the specified attribute from the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttributeNodeNS&amp;action=edit&amp;redlink=1" class="new"><b>setAttributeNodeNS</b></a>
</td>
<td>Sets an <a href="/w/index.php?title=dom/attributes&amp;action=edit&amp;redlink=1" class="new"><b>attribute</b></a> object as part of the object.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/setAttributeNS&amp;action=edit&amp;redlink=1" class="new"><b>setAttributeNS</b></a>
</td>
<td>Sets the value of the specified attribute within the specified namespace.
</td></tr></table><p> 
</p>
<h4>Properties</h4>
<p>The <b>media</b> object has these properties.
</p>
<table class="wikitable"><tr><th>Property
</th>
<th>Description
</th></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/audioTracks&amp;action=edit&amp;redlink=1" class="new"><b>audioTracks</b></a>
</td>
<td>Returns an <a href="/apis/audio-video/AudioTrackList"><b>AudioTrackList</b></a> object with the audio tracks for a given <b>video</b> element.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/autobuffer&amp;action=edit&amp;redlink=1" class="new"><b>autobuffer</b></a>
</td>
<td>The <a href="/w/index.php?title=apis/audio-video/properties/autobuffer&amp;action=edit&amp;redlink=1" class="new"><b>autobuffer</b></a> element is not supported by Internet Explorer 9. Use the <a href="/w/index.php?title=apis/audio-video/properties/preload&amp;action=edit&amp;redlink=1" class="new"><b>preload</b></a> element instead.
<p>This property is not supported for Metro style apps using JavaScript
</p>
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/autoplay&amp;action=edit&amp;redlink=1" class="new"><b>autoplay</b></a>
</td>
<td>Gets or sets a value that indicates whether to start playing the media automatically.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/buffered&amp;action=edit&amp;redlink=1" class="new"><b>buffered</b></a>
</td>
<td>Gets a collection of buffered time ranges.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/controls&amp;action=edit&amp;redlink=1" class="new"><b>controls</b></a>
</td>
<td>Gets or sets a flag that indicates whether the client provides a set of controls for the media (in case the developer does not include controls for the player).
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/currentSrc&amp;action=edit&amp;redlink=1" class="new"><b>currentSrc</b></a>
</td>
<td>Gets the address or URL of the current media resource (<b>video</b>,<b>audio</b>) that is selected by <b>IHTMLMediaElement</b>.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/currentTime&amp;action=edit&amp;redlink=1" class="new"><b>currentTime</b></a>
</td>
<td>Gets or sets the current playback position, in seconds.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/defaultPlaybackRate&amp;action=edit&amp;redlink=1" class="new"><b>defaultPlaybackRate</b></a>
</td>
<td>Gets or sets the default playback rate when the user is not using fast foward or reverse for a video or audio resource.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/duration&amp;action=edit&amp;redlink=1" class="new"><b>duration</b></a>
</td>
<td>Gets the duration, in seconds, of the current media resource, a <code>NaN</code> value if duration is not available, or <code>Infinity</code> if the media resource is streaming.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/ended&amp;action=edit&amp;redlink=1" class="new"><b>ended</b></a>
</td>
<td>Gets information about whether the playback has ended or not.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/error&amp;action=edit&amp;redlink=1" class="new"><b>error</b></a>
</td>
<td>Gets an <b>IHTMLMediaError</b> object representing the current error state of the media element.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/initialTime&amp;action=edit&amp;redlink=1" class="new"><b>initialTime</b></a>
</td>
<td>Gets the earliest possible position, in seconds, that the playback can begin.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/localName&amp;action=edit&amp;redlink=1" class="new"><b>localName</b></a>
</td>
<td>Retrieves the local name of the fully qualified XML declaration for a node.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/loop&amp;action=edit&amp;redlink=1" class="new"><b>loop</b></a>
</td>
<td>Gets or sets a flag that specifies whether playback should restart after it completes.
</td></tr><tr><td><b>msAudioCategory</b>
</td>
<td>Specifies the purpose of the audio or video media, such as background audio or alerts.
</td></tr><tr><td><b>msAudioDeviceType</b>
</td>
<td>Specifies the output device id that the audio will be sent to.
</td></tr><tr><td><b>msPlayToDisabled</b>
</td>
<td>Gets or sets whether the DLNA PlayTo device is available.
</td></tr><tr><td><b>msPlayToPrimary</b>
</td>
<td>Gets or sets the primary DLNA PlayTo device.
</td></tr><tr><td><b>msPlayToSource</b>
</td>
<td>Gets the source associated with the media element for use by the PlayToManager.
</td></tr><tr><td><b>msRealTime</b>
</td>
<td>Specifies whether or not to enable low-latency playback on the media element.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/muted&amp;action=edit&amp;redlink=1" class="new"><b>muted</b></a>
</td>
<td>Gets or sets a flag that indicates whether the audio (either audio or the audio track on video media) is muted.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/namespaceURI&amp;action=edit&amp;redlink=1" class="new"><b>namespaceURI</b></a>
</td>
<td>Retrieves the namespace URI of the fully qualified XML declaration for a node.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/networkState&amp;action=edit&amp;redlink=1" class="new"><b>networkState</b></a>
</td>
<td>Gets the current network activity for the element.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/paused&amp;action=edit&amp;redlink=1" class="new"><b>paused</b></a>
</td>
<td>Gets a flag that specifies whether playback is paused.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/playbackRate&amp;action=edit&amp;redlink=1" class="new"><b>playbackRate</b></a>
</td>
<td>Gets or sets the current speed for the media resource to play. This speed is expressed as a multiple of the normal speed of the media resource.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/played&amp;action=edit&amp;redlink=1" class="new"><b>played</b></a>
</td>
<td>Gets <a href="/w/index.php?title=apis/audio-video/HTMLTimeRanges&amp;action=edit&amp;redlink=1" class="new"><b>TimeRanges</b></a> for the current media resource that has been played.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/prefix&amp;action=edit&amp;redlink=1" class="new"><b>prefix</b></a>
</td>
<td>Retrieves the local name of the fully qualified XML declaration for a node.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/preload&amp;action=edit&amp;redlink=1" class="new"><b>preload</b></a>
</td>
<td>Gets or sets a hint to how much buffering is advisable for a media resource, even if <a href="/w/index.php?title=apis/audio-video/properties/autoplay&amp;action=edit&amp;redlink=1" class="new"><b>autoplay</b></a> is not specified.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/seekable&amp;action=edit&amp;redlink=1" class="new"><b>seekable</b></a>
</td>
<td>Returns a <a href="/w/index.php?title=apis/audio-video/HTMLTimeRanges&amp;action=edit&amp;redlink=1" class="new"><b>TimeRanges</b></a> object that represents the ranges of the current media resource that can be seeked.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/seeking&amp;action=edit&amp;redlink=1" class="new"><b>seeking</b></a>
</td>
<td>Gets a flag that indicates whether the the client is currently moving to a new playback position in the media resource.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/src&amp;action=edit&amp;redlink=1" class="new"><b>src</b></a>
</td>
<td>The address or URL of the a media resource (<b>video</b>, <b>audio</b>) that is to be considered.
</td></tr><tr><td><a href="/w/index.php?title=dom/properties/textContent&amp;action=edit&amp;redlink=1" class="new"><b>textContent</b></a>
</td>
<td>Sets or retrieves the text content of an object and any child objects.
</td></tr><tr><td><a href="/w/index.php?title=apis/audio-video/properties/volume&amp;action=edit&amp;redlink=1" class="new"><b>volume</b></a>
</td>
<td>Gets or sets the volume level for audio portions of the media element.
</td></tr></table><p> 
</p><p><br/></p>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li><code>Reference</code></li>
<li><code>audio</code></li>
<li><code>video</code></li></ul>
