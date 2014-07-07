{{Page_Title|Timing and performance standards}}
{{Flags
|State=In Progress
|Editorial notes=Needs table code fix in Notes
|Checked_Out=No
|High-level issues=Stub, Needs Topics, Missing Relevant Sections, Needs Review
|Content=Not Neutral, Compatibility Incomplete
}}
{{Summary_Section|This section documents the timing and performance-based standards supported by Windows Internet Explorer and Windows Store apps.}}
{{Basic Page}}
{{Standardization_Status|}}
{{API_Name}}


==Navigation Timing==

===Abstract===

This specification defines an interface for web applications to access timing information related to navigation and elements. 

The Navigation Timing API basically provides timings of all things going on from initiating navigating to another document (e.g. clicking a link, settings location.href) until the end of document onload event.

* Navigation Timing API Recommendation [http://www.w3.org/TR/navigation-timing/] (17 December 2012)
* Tutorial: Measuring page load speed with Navigation Timing [http://www.html5rocks.com/en/tutorials/webperformance/basics/]
* Browser Support: FF7+, Chrome6+, IE9+, Android Browser 4.0+, Mobile Chrome 33+ [http://caniuse.com/nav-timing]
* Polyfill: [http://nicj.net/usertiming-js/]

==Resource Timing==

===Abstract===

This specification defines an interface for web applications to access the complete timing information for resources in a document.

The Resource Timing API provides timings for all resources linked into a page.

* Resource Timing API Candidate Recommendation [http://www.w3.org/TR/resource-timing/] (25 March 2014)
* Tutorial: An Introduction to the Resource Timing API [http://calendar.perfplanet.com/2012/an-introduction-to-the-resource-timing-api/]
* Browser Support: FF15+, IE10, Chrome? (2012)

==User Timing==

===Abstract===

This specification defines an interface to help web developers measure the performance of their applications by giving them access to high precision timestamps.

Helps to get rid of Date.now() in performance measuring code. Can be used to measure random parts of code.

* User Timing API Recommendation [http://www.w3.org/TR/user-timing/] (12 December 2013)
* Tutorial: User Timing API [http://www.html5rocks.com/en/tutorials/webperformance/usertiming/]
* Polyfill: [https://gist.github.com/pmeenan/5902672]
* Browser Support: IE10+, Chrome25+, Android Browser 4.4+, Mobile Chrome 33+ [http://caniuse.com/user-timing]

==Page Visibility==

===Abstract===

This specification defines a means for site developers to programmatically determine the current visibility state of the page in order to develop power and CPU efficient web applications.

Enables developers to listen to visibility change event (e.g. user switches to another browser tab) and to determine visibility state of the page. Thus, expensive operations in means of performance can be stopped on invisible pages.

* Page Visibility API Recommendation [http://www.w3.org/TR/page-visibility/] (29 October 2013)
* Tutorial: Using the PageVisibility API [http://www.html5rocks.com/en/tutorials/pagevisibility/intro/]
* Browser Support: FF10+, IE10+, Chrome14+, Safari 6.1+, mobile Safari 7+, Android Browser 4.4+, Mobile Chrome 33+ [http://caniuse.com/pagevisibility]

==Animation Timing==

===Abstract===

This document defines an API web page authors can use to write script-based animations where the user agent is in control of limiting the update rate of the animation. The user agent is in a better position to determine the ideal animation rate based on whether the page is currently in a foreground or background tab, what the current load on the CPU is, and so on. Using this API should therefore result in more appropriate utilization of the CPU by the browser.

* Animation Timing API Recommendation [http://www.w3.org/TR/animation-timing/] (31 October 2013)
* Tutorial: The secret to silky smooth JavaScript animation! [http://creativejs.com/resources/requestanimationframe/]
* Browser Support: FF4+, Chrome10+, Safari 6+, mobile Safari 6+, Android Browser 4.4+, Mobile Chrome 33+  [http://caniuse.com/requestanimationframe]

==Efficient Script Yielding==

===Abstract===

This specification defines an interface for web applications to flush the browser event queue and receive an immediate callback.

* Efficient Script Yielding Editor's Draft [https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/setImmediate/Overview.html] (editor's draft, 28 July 2011)
* Browser Support: IE10+
{{Notes_Section
|Import_Notes====In this section===
{| class="wikitable"
|-
!Topic
!Description
|-
|Methods
|This section describes the methods associated with timing and performance standards supported by Internet Explorer and Metro style apps.
|-
|Objects
|This section describes the objects associated with timing and performance standards supported by Internet Explorer and Metro style apps.
|-
|Properties and Events
|This section describes the properties and events associated with timing and performance standards supported by Internet Explorer and Metro style apps.
|}
 
 
}}
{{Topics|Performance, Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}