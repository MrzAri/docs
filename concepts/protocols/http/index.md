---
title: 'HTTP'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTTP)'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
summary: 'HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.'
tags:
  - Basic_Pages
  - Web_Services
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'http/requesting resources'
    - 'http/resource metadata'
    - http/caching
    - 'http/access control'
    - 'http/state management'
    - 'http/content negotiation'
    - 'http/partial responses'
    - 'http/modifying resources'
    - 'http/conditional updates'
    - 'http/forms and scripts'
uri: concepts/protocols/http

---
<h2>Summary</h2>
<p>
HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.</p>
<h2>HTTP</h2>
<p>Hypertext Transfer Protocol (HTTP) is an application-layer protocol. HTTP is generally implemented on top of <tt><abbr title="Transmission Control Protocol, Internet Protocol">TCP/IP</abbr></tt> default port 80, but can be implemented on any interface supporting a duplex stream. It is used for exchanging messages (such has hypermedia documents) in between a client (a <i>user agent</i> like a browser or bot) and a server. The interactions are defined by a client-server model. The client sends a request to a server and the server sends back a response to the client.
</p><p>HTTP was one of the first protocols developed as part of Web starting in late 1989<sup id="cite_ref-1" class="reference"><a href="#cite_note-1">[1]</a></sup>, and later standardized over the course of many RFCs through the IETF.
</p>
<ul><li> <a href="/http/headers">List of HTTP headers</a></li>
<li> <a href="/http/methods">List of HTTP methods</a></li>
<li> <a href="/http/response_status_codes">List of HTTP status codes</a></li>
<li> HTTP the protocol: The entity-body and transfer control, what are resources</li>
<li> <a href="/concepts/Internet_and_Web/how_browsers_work#The_browser.27s_high_level_structure">Layered requests</a> with proxies and gateways</li>
<li> <a href="/w/index.php?title=http/requesting_resources&amp;action=edit&amp;redlink=1" class="new">Requesting resources</a>: GET, HEAD, OPTIONS</li>
<li> <a href="/w/index.php?title=http/resource_metadata&amp;action=edit&amp;redlink=1" class="new">Resource metadata</a>: Link, Last-Modified, Content-Type, Allow, etc</li>
<li> <a href="/w/index.php?title=http/caching&amp;action=edit&amp;redlink=1" class="new">Caching</a> and conditional requests</li>
<li> <a href="/w/index.php?title=http/access_control&amp;action=edit&amp;redlink=1" class="new">Access control</a></li>
<li> <a href="/w/index.php?title=http/state_management&amp;action=edit&amp;redlink=1" class="new">State management</a> with cookies</li>
<li> <a href="/w/index.php?title=http/content_negotiation&amp;action=edit&amp;redlink=1" class="new">Content negotiation</a>: Accept, Content-Location</li>
<li> <a href="/w/index.php?title=http/partial_responses&amp;action=edit&amp;redlink=1" class="new">Partial content responses</a></li>
<li> <a href="/w/index.php?title=http/modifying_resources&amp;action=edit&amp;redlink=1" class="new">Modification of resources</a>: PUT, PATCH</li>
<li> <a href="/w/index.php?title=http/conditional_updates&amp;action=edit&amp;redlink=1" class="new">Conditional updates</a></li>
<li> <a href="/w/index.php?title=http/forms_and_scripts&amp;action=edit&amp;redlink=1" class="new">Forms and scripts</a>: POST with HTML Forms, using 3xx Status codes</li></ul><h3>An HTTP Request</h3>
<p>HTTP is a plain-text protocol in the style of MIME (used by Email). An HTTP request begins with a client making a request to a server. The request contains a <i>request-line</i> identifying a <a href="/http/methods">method</a>, the name of a resource, and the HTTP version of the request. This is followed by a number of <a href="/http/headers">header lines</a>, then a blank line, and an optional request-body.
</p><p>The server response is similar: It responds with the status-line consisting of the HTTP version, followed by a 3-digit numeric <a href="/http/response_status_codes">status code</a> and a status message. This is followed by a number of header lines, blank line, and optional response-body.
</p><p>Lines are terminated with a carriage-return line-feed (CRLF, or "\r\n").
</p><p>An example HTTP request will look like:
</p>
<pre>GET / HTTP/1.1
Host: example.com
User-Agent: ExampleUA/4.0
Accept: */*

</pre>
<p>To which the server might reply:
</p><p><br/></p>
<pre>HTTP/1.1 200 OK
Date: Thu, 17 Jul 2014 15:08:35 GMT
Expires: Fri, 18 Jul 2014 15:08:35 GMT
Cache-Control: public
Content-Type: text/plain;charset=UTF-8
Server: ExampleServer/4.0
Content-Length: 74

Hypertext Transfer Protocol (HTTP) is an application-layer protocol. ...
</pre>
<p>Some of the most common headers include:
</p>
<dl><dt> Host </dt>
<dd> Provides the hostname for supporting multiple hostnames on a single server. For backwards compatibility, this is required even if the request is made in absolute form.</dd>
<dt> User-Agent </dt>
<dd> A string identifying the version of software making the request</dd>
<dt> Accept </dt>
<dd> Informs the server of which media-types the user agent would like to see, used for Content-Type negotiation</dd>
<dt> Date </dt>
<dd> Indicates what date/time the message originated.  Required in responses.</dd>
<dt> Expires </dt>
<dd> A caching header which indicates the time after which the resource will be "stale".</dd>
<dt> Cache-Control </dt>
<dd> A caching header that can describe who is allowed to cache the resource and for how long</dd>
<dt> Server </dt>
<dd> A string identifying the version of the server responding to the request</dd>
<dt> Content-Type </dt>
<dd> Indicates the media type (MIME type) of the attached entity body, if any.</dd>
<dt> Content-Length </dt>
<dd> Indicates the length of the attached entity body, if any.</dd></dl><h3>Design of HTTP</h3>
<p>HTTP follows a number of patterns to give it well-defined functionality for the benefit of clients and servers:
</p>
<ul><li> it is <i>client-server</i>, which separates data storage concerns from user interface concerns;</li>
<li> it is <i>layered</i>, to allow intermediate processing steps along the network path;</li>
<li> it is <i>stateless</i>, so server load is proportional with the number of requests instead of the total number of users; and</li>
<li> it is <i>cachable</i>, to enhance scalability and network performance.</li></ul><h3>History of HTTP</h3>
<h4>List of Specifications</h4>
<ol><li> Informally implemented since 1991</li>
<li> HTTP/1.0, May 1996 <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc1945">RFC1945</a></li>
<li> HTTP/1.1 first revision, January 1997 <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc2068">RFC2068</a></li>
<li> HTTP/1.1, second revision June 1999 <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc2616">RFC2616</a></li>
<li> HTTP/1.1, third revision June 2014 <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc7230">RFC7230</a> <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc7231">RFC7231</a> <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc7232">RFC7232</a> <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfc7233">RFC7233</a> <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfcC7234">RFC7234</a> <a rel="nofollow" class="external text" href="http://tools.ietf.org/html/rfcC7235">RFC7235</a></li></ol><p><br/></p><p><br/></p>
<h2>References</h2>
<ol class="references"><li id="cite_note-1"><span class="mw-cite-backlink"><a href="#cite_ref-1">↑</a></span> <span class="reference-text"><a rel="nofollow" class="external free" href="http://webfoundation.org/about/vision/history-of-the-web/">http://webfoundation.org/about/vision/history-of-the-web/</a></span>
</li>
</ol>
