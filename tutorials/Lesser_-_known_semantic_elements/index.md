== Introduction ==
 
In this article of the [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum] we will look at some of the more obscure
and less well-known and used semantic elements in HTML. We’ll look
at marking up programming code, interaction with computers,
citations and abbreviations, showing changes made to documents and 
more.
 
'''Note''': You can [http://dev.opera.com/articles/view/21-lesser-known-semantic-elements/lesserknownsemantics.html view all the examples running live]

== Highlighting contact information ==
 
The <code>&lt;address&gt;</code> element is probably the most badly named and
misunderstood element in HTML. At first glance, with a name like
“address” it would appear that it is used to encapsulate addresses,
email, postal or otherwise. This is only partially the case.
 
The actual meaning of <code>&lt;address&gt;</code> is to supply contact information ''for the author or authors'' of the page, or the major section of the page, that it
appears within. This can take the form of a name, an email address, a
postal address or a link to another page with more contact
information. For example:
 
<pre>&lt;address&gt; 
  &lt;span&gt;Mark Norman Francis&lt;/span&gt;, 
  &lt;span class="tel"&gt;1-800-555-4865&lt;/span&gt;
&lt;/address&gt;
</pre>

In the following example, the address is contained within the footer
paragraph and simply links to another page on the site. The extended
contact information on the page that this link targets could then
have much more detailed contact information, to save repeating it
endlessly across the entire site.
 
<pre>&lt;footer&gt;
&lt;p&gt;© Copyright 2011&lt;/p&gt;
&lt;address&gt;
&lt;a href="/contact/"&gt;Mark Norman Francis&lt;/a&gt;
&lt;/address&gt;
&lt;/footer&gt;</pre>

Of course, if the site had more than one author, the same pattern
could be used, just linking to different contact pages for the
different authors.
 
It is *incorrect* to use the <code>&lt;address&gt;</code> element to indicate any other
type of addresses, such as this:
 
<pre>&lt;p&gt; Our company address: &lt;/p&gt;
  &lt;address&gt;
    Opera Software ASA,
    Waldemar Thranes gate 98,
    NO-0175 OSLO,
    NORWAY
  &lt;/address&gt;
</pre>

(Of course, if Opera was taking collective responsibility for
this article, this would be correct, even though Opera is not the author of this particular page.)

For any general address, you can use something called a "microformat"
to indicate that a paragraph contains an address. There is [http://dev.opera.com/articles/html/ more information on Microformats on dev.opera.com]].

== Programming languages and code ==
 
The <code>&lt;code&gt;</code> element is used to indicate computer code or programming
languages, such as PHP, JavaScript, CSS, XML and so on. For short
samples within a sentence, you would simply wrap the element around
the code snippet, like so:
 
<pre>&lt;p&gt;It is bad form to use event handlers like
&lt;code&gt;onclick&lt;/code&gt; directly in the HTML.&lt;/p&gt;
</pre>

For larger samples of code which span multiple lines, you can use a 
preformatted block as shown in the [http://www.w3.org/wiki/Marking up textual content in HTML] article.
 
Although there is no defined method of indicating which programming
language or code is shown within the <code>&lt;code&gt;</code> element, you can use
the <code>class</code> attribute. A common practice (mentioned
in the HTML 5 specification) is to use the prefix <code>&lt;language-&gt;</code> and then append
the language name. So the above example would become:
 
<pre>&lt;p&gt;It is bad form to use event handlers like 
&lt;code class="language-javascript"&gt;onclick&lt;/code&gt;
directly in the HTML.&lt;/p&gt;
</pre>

Some programming languages have names that cannot be easily
represented in classes, such as C# (C-Sharp). The correct way of
writing this would be “<code>&lt;class='language-c\#'&gt;</code>”, which could be confusing
and easily mis-typed. I would recommend using a class consisting of
only letters and hyphens, and spelling it out completely. So in this
case, use “<code>&lt;class='language-csharp'&gt;</code>” instead.

== Displaying computer interaction ==
 
The two elements <code>&lt;samp&gt;</code> and <code>&lt;kbd&gt;</code> can be used to indicate the input
and output of interaction with a computer program. For example:
 
<pre>&lt;p&gt;One common method of determining if a computer is connected
to the internet is to use the computer program &lt;code&gt;ping&lt;/code&gt;
to see if a computer likely to be running is reachable.&lt;/p&gt;

&lt;pre&gt;&lt;samp class="prompt"&gt;kittaghy%&lt;/samp&gt; &lt;kbd&gt;ping -o google.com&lt;/kbd&gt;
  &lt;samp&gt;PING google.com (64.233.187.99): 56 data bytes
  64 bytes from 64.233.187.99: icmp_seq=0 ttl=242 time=108.995 ms

  --- google.com ping statistics ---
  1 packets transmitted, 1 packets received, 0% packet loss
  round-trip min/avg/max/stddev = 108.995/108.995/108.995/0.000 ms
  &lt;/samp&gt;&lt;/pre&gt;
</pre>

The <code>&lt;samp&gt;</code> element indicates sample output from a computer program. As 
shown in the example, different types of output can be indicated using
the <code>class</code> attribute. There are no widely adopted conventions for which
kind of classes to use, however.
 
The <code>&lt;kbd&gt;</code> element indicates input from the user interacting with the
computer. Although this is traditionally keyboard input (hence the
“kbd” contraction used) it should also be used to indicate other
types of input, such as spoken voice.

== Variables ==
 
The <code>&lt;var&gt;</code> element is used to indicate variables in textual content.
This can include algebraic mathematical expressions or within
programming code. For example:
 
<pre>&lt;p&gt;The value of &lt;var&gt;x&lt;/var&gt; in
 3&lt;var&gt;x&lt;/var&gt;+2=14 is 4.&lt;/p&gt;
    
&lt;pre&gt;&lt;code class="language-perl"&gt;
my &lt;var&gt;$welcome&lt;/var&gt; = "Hello world!";
&lt;/code&gt;&lt;/pre&gt;
</pre>

== Citations ==
 
The <code>&lt;cite&gt;</code> element is used to indicate where the nearby content comes
from—when quoting a person, a book or other publication, or
generally referring people to another source, that source should be
wrapped in a <code>&lt;cite&gt;</code> element. For example:
 
<pre>&lt;p&gt;The saying &lt;q&gt;Everything should be made as simple as possible,
but not simpler&lt;/q&gt; is often attributed to &lt;cite&gt;Albert
Einstein&lt;/cite&gt;, but it is actually a paraphrasing of a quote which
is much less easy to understand.&lt;/p&gt;
</pre>

== Abbreviations ==
 
The <code>&lt;abbr&gt;</code> element is used to indicate where 
abbreviations occur, and provide a method for expanding upon them
without unnecessarily interrupting the flow of the document.
 
The text that is the abbreviation gets wrapped in the <code>&lt;abbr&gt;</code> element, 
and the full expansion is placed in the <code>title</code> attribute, like so:
 
<pre>&lt;p&gt;Styling is added to 
&lt;abbr title="Hypertext Markup Language"&gt;HTML&lt;/abbr&gt; documents
using &lt;abbr title="Cascading Style Sheets"&gt;CSS&lt;/abbr&gt;.&lt;/p&gt;
</pre>

Note that in the HTML4 specification there is also an element called <code>&lt;acronym&gt;</code>, which had a similar function to <code>&lt;abbr&gt;</code>, but for acronyms. This was dropped in HTML5, because the functional difference between an acronym and an abbreviation isn't distinct enough to require different elements.

One problem with this is Internet Explorer support: Internet Explorer (before version 7, and 7 doesn't provide the dotted underline underneath abbreviations that other browsers do) doesn't recognise the <code>&lt;abbr&gt;</code> element, but does recognise <code>&lt;acronym&gt;</code>.  But this is easy enough to get around. To ensure that <code>&lt;abbr&gt;</code> will be stylable in Internet Explorer, you simply need to create the element with JavaScript. Put this code in your document <code>&lt;head&gt;</code>:

<pre>&lt;script type="text/javascript"&gt;document.createElement('abbr');&lt;/script&gt;</pre>

To find out more about why this works, read [[HTML structural elements#HTML5_element_support]]. Of course, you could just stick to using <code>&lt;acronym&gt;</code> for now, until you decide to make a complete move towards using HTML5.

== Defining instances ==
 
There is some confusion over the proper use of <code>&lt;dfn&gt;</code>, which is
described in the HTML specification as “the defining instance of the
enclosed term”. This is remarkably close to the idea of the <code>&lt;dt&gt;</code> element (definition term) used in definition lists.
 
The difference is that the term used in <code>&lt;dfn&gt;</code> does not have to be 
a part of a list of terms and descriptions and can instead be used
as part of the normal flow of text, even in conversational style
prose. So, let's look at an example of using <code>&lt;dfn&gt;</code>:
 
<pre>&lt;p&gt;&lt;dfn&gt;HTML&lt;/dfn&gt;: HTML stands for "HyperText Markup Language". This is 
the language used to describe the contents of web documents.&lt;/p&gt;
</pre>
 
The term HTML appears, and is followed immediately by a definition of what it is, therefore this is an ideal place for the <code>&lt;dfn&gt;</code> eement to be used. You should only really use it once on a page, where a term is first defined, but terms should only really be defined once on a page anyway, so this is not too troubling.
 
This is all well and good, but an isolated example is not very practical - the use of <code>&lt;dfn&gt;</code> is recommended when an abbreviation is used more than
once on a page. For example, in the article [[The basics of HTML]] earlier in
this series, the abbreviation HTML appeared over forty times. To
use the code “<code>&lt;abbr title="HyperText Markup Language"&gt;HTML&lt;/abbr&gt;</code>” 
each and every time it is used would be a waste of bandwidth, 
visually distracting and for screen reader users probably quite
tiresome as HTML is expanded over and over, even though they would
already have been told what it stands for. Instead, the code could
be inserted at the point where it is first defined for the readers:
 
<pre>&lt;p&gt;&lt;dfn&gt;&lt;abbr&gt;HTML&lt;/abbr&gt;&lt;/dfn&gt; ("HyperText Markup Language") is 
a language to describe the contents of web documents.&lt;/p&gt;
</pre>

Then later, whenever HTML is used, it can be marked up simply as 
“<code>&lt;abbr&gt;HTML&lt;/abbr&gt;</code>”. A user agent could then make available to the
user some method of retrieving the defining instance of that
abbreviation. Unfortunately, no user agent currently does this, 
including screen readers. It would be better, then, to use the 
<code>title</code> attribute as well to provide this information:
 
<pre>&lt;p&gt;&lt;dfn&gt;&lt;abbr title="HyperText Markup Language"&gt;HTML&lt;/abbr&gt;&lt;/dfn&gt; ("HyperText Markup Language") is a language to describe the contents of web documents.&lt;/p&gt;
</pre>

Unfortunately, we have now doubled up on the expanded term for HTML,
which can be a problem for screen reader users. However, leaving out
the visible expansion makes the document less useful for sighted
users which will be the greater proportion of users in almost every
case.
 
I would suggest that this is an acceptable trade-off when there are
only one or two items requiring a definition (in pages that require a larger number of definitions, it might be
better to create a glossary section or page where the more rigourous
definition list markup can be used). If you are very 
concerned about this, the code could instead appear as:
 
<pre>&lt;p&gt;&lt;abbr title="HyperText Markup Language"&gt;HTML&lt;/abbr&gt; 
(&lt;dfn&gt;HyperText Markup Language&lt;/dfn&gt;) is a language to 
describe the contents of web documents.&lt;/p&gt;</pre>
 
However, the user
agent would still have to have some method of connecting the definition with all the instances of the defined term. No browser currently does anything useful with <code>&lt;dfn&gt;</code>, although it is still a useful hook for CSS to style. The solution suggested above is currently the best we’ve got.
 
This is an unfortunate instance where the specification has been
created without clear guidelines on how an element is supposed to be
used, and probably was not based upon any real-world usage of that
element — otherwise there would be a method of combining the
term with its full description or definition. The HTML 5 
specification goes into a lot more [[http://www.whatwg.org/specs/web-apps/current-work/multipage/text-level-semantics.html#the-dfn-element detail about how dfn is to be used]], but this is still in draft and not suitable for use on the
web yet.

== Superscript and subscript ==
 
To mark up a part of some text as being super- or subscripted 
(slightly raised or lowered compared to the rest of the text) 
you use the <code>&lt;sup&gt;</code> and <code>&lt;sub&gt;</code> elements.
 
Some languages require these elements for correct usage of
abbreviations and it can be used when a small amount of mathematical
content is being marked up, without resorting to using MathML (a
specific, rather heavyweight mathematical markup language, created
for the sole purpose of marking up heavyweight mathematical
formulae).
 
An example of both types:
 
<pre>&lt;p&gt;The chemical formula for water is H&lt;sub&gt;2&lt;/sub&gt;O, and it
is also known as hydrogen hydroxide.&lt;/p&gt;
&lt;p&gt;The famous formula for mass-energy equivalence as derived
by Albert Einstein is E=mc&lt;sup&gt;2&lt;/sup&gt; — energy 
is equal to the mass multiplied by the speed of light 
squared.&lt;/p&gt;
</pre>

== Line breaks ==
 
Because of the way HTML defines white space, it is not possible
to control where lines of text break (such as marking up a postal 
address as a paragraph, but wanting the visual appearance to have
each part of the address appear on a separate line) by simply 
pressing the Return key whilst writing the text.
 
A line break can be introduced into the document using the <code>&lt;br&gt;</code>
element. However, this should only be used to force line breaks where
they are required, and never to apply more vertical spacing between
paragraphs or such in a document — that is more properly done
with CSS.
 
Sometimes it might be easier to use the preformatted text block
rather than inserting <code>&lt;br&gt;</code> elements. Or, if one particular part
of some text is desired to be on a line by itself, but this is
just a styling issue, it can be surrounded by a <code>&lt;span&gt;</code> element
and set to display as a block level element.
 
So for example you could write the Opera contact address seen
earlier in this article when talking about the <code>&lt;address&gt;</code> element like
this instead:
 
<pre>&lt;p&gt;Our company address: &lt;/p&gt;
&lt;address&gt;
Opera Software ASA,&lt;br&gt;Waldemar Thranes gate 98,&lt;br&gt;
NO-0175 OSLO,&lt;br&gt;NORWAY
&lt;/address&gt;
</pre>

Of course, if you are writing XHTML syle syntax rather than HTML, the element
should be self-closing, like so: &lt;br /&gt;.

== Horizontal rules ==
 
A horizontal rule is created in HTML with the <code>&lt;hr&gt;</code> element. It 
inserts into the document a line, which is described to represent
a boundary between different sections of a document.
 
Whilst some argue that this is inherently non-semantic and purely
a visual, presentational effect, there is actually some precedent
in literature for such an element to exist. Within a chapter (which
could be described as a section within a book), a horizontal rule
will appear between scenes that occur in different times and/or 
places. Also, poetry can use decorative breaks to separate different
stanzas of the poem.
 
Neither use would justify the existence of a new header element,
which is the accepted way of marking the boundaries between document
sections.
 
The <code>&lt;hr&gt;</code> element has no uncommon attributes and should be styled
using CSS if the default appearance in unsatisfactory.
 
Also, like the line break, if you are writing XHTML style syntax and not HTML,
use the self-closing form — &lt;hr /&gt;.
 
== Changes to documents (inserting, deleting and outdated content) ==
 
If a document has been changed since the first time it was available,
you can mark these changes so that return visitors or automated
processes can tell what has changed, and when.
 
New text (insertions) should be surrounded by the <code>&lt;ins&gt;</code> element. 
Text that has been removed (deletions) should be surrounded by the
<code>&lt;del&gt;</code> element. If a deletion
and insertion have been made at the same point in the document, good form suggests
having the deleted text first, followed by the insertion.
 
Both elements can take two attributes that give more meaning to the
edits.
 
If the reason for the change is stated in the page or elsewhere on
the web, you should link to that document or fragment in the <code>cite</code>
attribute. This effectively says “This change happened because of
this reason.”
 
You can also indicate the time at which the change was made by
using a <code>datetime</code> attribute. The value should be an ISO-standard
timestamp, which is generally of the form “YYYY-MM-DD HH:MM:SS
±HH:MM” ([http://en.wikipedia.org/wiki/ISO_8601 more information is available on wikipedia]).
 
An example using both attributes:
 
<pre>&lt;p&gt;We should only solve problems that actually arise. As
  &lt;cite&gt;&lt;del datetime="2008-03-25 18:26:55 Z"
  cite="/changes.html#revision-4"&gt;Donald Knuth&lt;/del&gt;&lt;ins
  datetime="2008-03-25 18:26:55 Z"
  cite="/changes.html#revision-4"&gt;C. A. R. Hoare&lt;/ins&gt;&lt;/cite&gt;
  said: &lt;q&gt;premature optimization is the root of all 
  evil&lt;/q&gt;.&lt;/p&gt;</pre>


In addition, we can also use the <code>&lt;s&gt;</code> element to markup content that is outdated, perhaps if you want to mark it for updating or deletion. For example:

<pre>&lt;p&gt;&lt;s&gt;The president of the USA is currently George W. Bush&lt;/s&gt;.&lt;/p&gt;</pre>

== Summary ==
 
In this article, we have discussed some of the lesser known and more
infrequently used semantic elements available in HTML. 

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [http://dev.opera.com/articles/view/21-lesser-known-semantic-elements/ 21: Lesser-known semantic elements], written by Mark Norman Francis. Like the original, it is published under the [http://creativecommons.org/licenses/by-nc-sa/2.5/ Creative Commons Attribution, Non Commercial - Share Alike 2.5] license.

[[Category:Tutorials]]
[[Category:WSC]]
[[Category:HTML]]