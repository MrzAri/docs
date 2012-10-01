{{Page_Title|The HTML <head>}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article covers the most common parts that can be included in the <code>&lt;head&gt;</code> section of HTML documents. Making sure that all of these are correct will result in your document being fast, and easy to find and understand.}}
{{Tutorial
|Content=== Introduction ==
 
This article deals with a part of the HTML document that does not get the attention it deserves: the markup that goes inside the <code>head</code> element. By the end of this tutorial you’ll have learnt about the different parts of this section and what they all do, including the <code>title</code> element, keywords and description (which are handled by <code>meta</code> elements) and more. You’ll also learn about JavaScript and CSS styles (both internal and external) and about what not to leave in the <code>head</code>. You can [http://dev.opera.com/articles/view/13-the-html-head-element/headtutorial.zip download some demo files here], which we will refer to during the article; feel free to play with them however you like once you have finished working through it. Make sure you go through the full tutorial from start to finish, as it builds up a series of best practices to follow when dealing with the HTML <code>head</code>. Whilst each part is valid in itself, there is a conclusion at the end about the best practices that will make you reconsider some of the earlier advice.

== Head? What head are we talking about? ==
 
The <code>body</code> (the <code>&lt;body&gt;&lt;/body&gt;</code> tags and everything in between) is where you’ll spend most of your time as a web designer or developer, as this is where all the content of the document goes. The <code>head</code> (the <code>&lt;head&gt;&lt;/head&gt;</code> tags and everything in between) plays a seemingly less important role because, with the exception of the <code>title</code> element, nothing you put in this part of the document is directly visible to your site’s visitors. Instead, the <code>head</code> is the place where most of the instructions for the browser are located and where you store extra information — so called <code>meta</code> information — about the document.

== Setting the document’s primary language ==
 
One piece of information about the document goes on the parent of the <code>head</code>, the <code>html</code> element. It is here that we define the primary natural language of the document. By natural language, we mean ''human'' language, such as French, Thai or even English. This helps screen readers, because for example the word "six" is pronounced very differently in French and English. It's a good idea to define the primary language of a document, especially when you are writing pages for an international audience; you don't tend to see that many pages that use it, however. You set it as follows:
 
<pre>&lt;html lang="en-GB"&gt;
  ...
&lt;/html&gt;</pre>

If you don't do it, Google along with other search engines might find it difficult to crawl your site, or take longer than anticipated.
 
Note that you can also set the language of sub sections of your document by using the <code>lang</code> attribute on other elements, for example <code>&lt;span lang="fr"&gt;Bonjour&lt;/span&gt;</code>.
 
The attributes you use to set the language depend on the <code>doctype</code> of your document. The [http://www.w3.org/TR/i18n-html-tech-lang/#ri20040429.092928424 W3C says]

 <blockquote>For HTML use the <code>lang</code> attribute only, for XHTML 1.0 served as text/html use the  <code>lang</code>  and  <code>xml:lang</code>  attributes, and for XHTML served as XML use the  <code>xml:lang</code>  attribute only.</blockquote> 

The language codes may be two-letter codes, such as <code>en</code> for English, four-letter codes such as <code>en-US</code> for American English, or other, less common, codes. The two-letter codes are defined in [http://en.wikipedia.org/wiki/ISO_639-1 ISO 639-1], although modern best practice dictates that you should [http://www.w3.org/International/articles/language-tags/ use the IANA subtag registry for your language code definitions].

==Setting your document's character encoding==

One new feature HTML5 includes is a special element for setting the character encoding of your documents: the range of different characters you want to use. It looks like so: 

<pre>&lt;meta charset="utf-8" /&gt;</pre>

Don't worry too much about this for now. <code>utf-8</code> is the universal character encoding, which includes pretty much any character that you might want to use on a web page, from any common human language, so it is a good idea to declare this to make sure you HTML has full international capabilities. In addition, you can avoid a [http://code.google.com/p/doctype/wiki/ArticleUtf7 serious Internet Explorer security risk] by declaring it in the first 512 bytes of the page. So just below the <code>&lt;head&gt;</code> tag is fine. This is what all the below examples will do.

== Judging a document by its title ==
 
One of the most important elements in the <code>head</code> is the <code>title</code>. The text contained within the <code>title</code> is displayed by pretty much all user agents/browsers in the browser application title bar (the bar bordering the top of the browser window. It is the first piece of content that web users will see when they visit your site, and therefore it is very important. In addition, assistive technologies like screen readers (software that reads out web pages to users with visual impairments) give this as a first hint of what visitors can expect from the document, and a lot of search engines work similarly too, so your chances to get found on the web increase drastically when you use a good title that is human readable and contains the right keywords. Let’s take the following HTML document ([http://dev.opera.com/articles/view/13-the-html-head-element/headexample.html headexample.html] in your zip file) and open it in a browser.
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;I am a title example&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
You’ll see that the text in the <code>title</code> is displayed in the bar above the browser navigation as shown in Figure 1.

[[Image:Head-fig.gif|The title is displayed in the title bar of the web browser]] 

Figure 1: Displaying a title in a browser.
 
There are many tutorials on the Web about how to write good document titles, most of which are related to search engine optimization (SEO). Don’t get overboard and try to trick the search engines into showing up an inflated number of search results. Write a concise short information piece about what the document is. “Breeding Dogs — Tips about Alsatians” is a lot more human digestible than “Dogs, Alsatian, Breeding, Dog, Tips, Free, Pet.”

== Adding keywords and a description ==
 
The next thing to do might seem superfluous at first as it will never be directly visible to your visitors: adding a description and keywords. Both of these get added to the <code>head</code> inside <code>meta</code> elements, as shown in the following example taken from the Yahoo! Eurosport site ([http://dev.opera.com/articles/view/13-the-html-head-element/headwithmeta.html headwithmeta.html]):
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;Yahoo! UK &amp; Ireland Eurosport—Sports News
|Sport&lt;/title&gt;
  &lt;meta name="description" content="Latest sports news and live scores from Yahoo! Eurosport UK. Complete sport coverage with Football results, Cricket scores, F1, Golf, Rugby, Tennis and more."&gt;
  &lt;meta name="keywords" content="eurosport,sports,sport,sports news,live scores,football,cricket,f1,golf,rugby,tennis,uk,yahoo"&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
If you open this document in a browser you’ll not see anything in the <code>body</code> of the document, however, if you put this document online and search engines index it, the description will be displayed as the text below the link in search engine results, as shown in Figure 2.

[[Image:head-fih.gif|descriptions showing in a search engine results page]] 

Figure 2: Descriptions show up in search engine result pages.
 
This could be the crucial bit of information a possible visitor of your site was looking for and the reason for him or her to click the link. Descriptions have another use too — some browsers show the description as extra information when you add the document to your favourites, as shown in Figure 3:

[[Image:head-fii.gif|Some browsers use the description as a bookmark description]] 

Figure 3: Descriptions show up in some browsers when you add the document as a favourite.
 
So although there is no obvious immediate benefit to adding meta descriptions, they do play an important role in the success of your document. The same — to a smaller degree — applies to the keywords you added.
 
Although years of abuse by spammers made search engines not take keywords seriously any more, they can however still be a really good tool to use if you want to quickly index a lot of documents without having to scan and analyze the content. You could use the <code>meta</code> keywords for example in a content management system by writing a script that indexes them and makes your search engine a lot faster. It doesn’t hurt to provide a way of finding documents without having to analyze their content. By adding some keywords in a <code>meta</code> element you leave yourself the option to have a clever and fast search for your sites should you want to create something like this in the future. Think of keywords as small bookmarks you leave in a massive book to make it easier for yourself to find a certain section immediately without having to read through whole chapters.

== What about the looks? Adding styles ==
 
The next thing you can add to the <code>head</code> of a document is style rules, defined in Cascading Style Sheets (CSS). You can embed those directly in the <code>head</code> using a <code>style</code> element, for example ([http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestyles.html headinlinestyles.html]):
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;Breeding Dogs—Tips about Alsatians&lt;/title&gt;
  &lt;meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed."&gt;
  &lt;meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet"&gt;
  &lt;style type="text/css"&gt;
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Test!&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
If you open this in a browser it’ll show the “Test!” text in grey on a black background, and the font will be Helvetica or Arial, depending what your system has installed. The <code>style</code> element can also contain another attribute called <code>media</code>, which defines what kind of media will use these styles, ie do you want these styles used when viewing the document on a computer screen, on a handheld device, or when printed out? There are several media types to choose from, the most useful being:
 
* <code>screen</code> — for displaying on monitors.
* <code>print</code> — to define what a printout of the document should look like.
* <code>handheld</code> — to define the look and feel of the document on mobile devices and other handheld devices.
* <code>projection</code> — for presentations done in HTML, for example supported by the [http://www.opera.com/support/tutorials/operashow/ Opera Show feature].
 
If you for example want to override the colours used on the screen and use a larger font size to make the page better for printing, you can add another style block below the first one, with a <code>media</code> attribute of <code>print</code>, as seen below (check out the full code in [http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestylesmedia.html headinlinestylesmedia.html]):
 
<pre>&lt;style type="text/css" media="print"&gt;
  body{
    background:#fff;
    color:#000;
    font-family: helvetica, arial, sans-serif;
    font-size:300%;
  }
&lt;/style&gt;</pre>
 
Now when you go to print this web page, the browser knows to use the print stylesheet for printing the document, and not the screen styles. Check this out by loading [http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestylesmedia.html headinlinestylesmedia.html] and selecting print preview, as shown in Figure 4:

[[Image:head-fij.gif|The same page with print and screen style sheets applied]] 

Figure 4: A screen and a print style sheet.

== Adding dynamic features using JavaScript ==
 
Another thing you can add to the <code>head</code> is scripts that get executed by the browser — so called “client side scripts” — written in JavaScript. As you learned in [http://www.w3.org/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript Article 4], JavaScript adds dynamic behavior to the static HTML document, for example animation effects, or form data validation, or other things being triggered when the user performs certain actions.
 
You add JavaScript to a document using the <code>script</code> element. When a browser encounters one of these, it’ll drop everything else and pause parsing of the rest of the document while it tries to execute the code inside it. This means that when you want to make sure that your JavaScript is available before the main document loads, you need to add it to the <code>head</code>. For example, you can give the visitor a warning that a certain link will take them to another server with the following script ([http://dev.opera.com/articles/view/13-the-html-head-element/headscript.html headscript.html]):
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;Breeding Dogs—Tips about Alsatians&lt;/title&gt;
  &lt;meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed."&gt;
  &lt;meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet"&gt;
  &lt;style type="text/css" media="screen"&gt;
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
    a {color:#fff}
  &lt;/style&gt;
  &lt;style type="text/css" media="print"&gt;
    body{
      background:#fff;
      color:#000;
      font-family: helvetica, arial, sans-serif;
      font-size:300%;
    }
  &lt;/style&gt;
  &lt;script&gt;
    function leave(){
      return confirm("This will take you to another site,\n are you sure you want to go?")
    }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
Test!
&lt;a href="http://dailypuppy.com" onclick="return leave()"&gt;The Daily Puppy&lt;/a&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
If you open this example in your web browser and click the link you’ll get asked to confirm your action. This is just a quick example of scripting and is far from what is best practice these days. Other tutorials later on in this course will deal with JavaScript best practices and teach you JavaScript techniques in depth, but don’t worry about it for now.

== Stop right there! Inline CSS and JavaScript is not too clever! ==
 
Strong words, yes, but there is one thing you need to remember when you build web sites: the best thing to do is to re-use your code as much as possible. Adding site-wide styles and scripts into each and every one of your pages doesn’t make much sense — on the contrary, it makes it harder to maintain a complete site and bloats the individual documents unnecessarily.
 
It is much better to put your styles and scripts in external files, and import them into your HTML files where needed, so you only need to update them in one place if changes need to be made. For your JavaScript, you do this using <code>script</code> elements that have no script inside them, but instead link to an external file using a <code>src</code> attribute, as seen in the code below ([http://dev.opera.com/articles/view/13-the-html-head-element/externaljs.html externaljs.html]):
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;Breeding Dogs—Tips about Alsatians&lt;/title&gt;
  &lt;meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed."&gt;
  &lt;meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet"&gt;
  &lt;style type="text/css" media="screen"&gt;
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
    a {color:#fff}
  &lt;/style&gt;
  &lt;style type="text/css" media="print"&gt;
    body{
      background:#fff;
      color:#000;
      font-family: helvetica, arial, sans-serif;
      font-size:300%;
    }
  &lt;/style&gt;
  &lt;script src="leaving.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
Test!
&lt;a href="http://dailypuppy.com" onclick="return leave()"&gt;The Daily Puppy&lt;/a&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
It is not as easy with CSS. The <code>style</code> element does not have a <code>src</code> attribute, so you need to use the <code>link</code> element instead — it has an <code>href</code> attribute that specifies an external CSS file to import, and a <code>media</code> attribute to define if these styles should be used for screen, print etc, similar to what we saw earlier on. By putting both CSS and JavaScript into their own files you can cut down the length of the <code>head</code> immensely, as shown below ([http://dev.opera.com/articles/view/13-the-html-head-element/externalall.html externalall.html]):
 
<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;Breeding Dogs—Tips about Alsatians&lt;/title&gt;
  &lt;meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed."&gt;
  &lt;meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet"&gt;
  &lt;link rel="stylesheet" type="text/css" media="screen" href="styles.css"&gt;
  &lt;link rel="stylesheet" type="text/css" media="print" href="printstyles.css"&gt;
  &lt;script src="leaving.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
Test!
&lt;a href="http://dailypuppy.com" onclick="return leave()"&gt;The Daily Puppy&lt;/a&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
 
The other benefits of keeping styles and scripts in their own files are:

# You make it both faster and easier for your site visitors, because although a few extra files are downloaded, the style and script information doesn't need to be repeated in each web page file (it is just downloaded once, in the separate script/style files) so each page file downloaded will be smaller. In addition, the CSS and JavaScript files will be cached (stored temporarily on your local machine), so that the next time you access the site, the files will be on your computer already, meaning they don’t need to be downloaded again.
# Next comes ease of maintenance. The style and script for the whole site — which could be thousands of documents — are in one single location, so if you need to change something you only need to change one file, and not thousands.
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections==== Exercise questions ===
 
* Why does it make sense to add a description in a <code>meta</code> element if it doesn’t get displayed on the screen?
* What is the benefit of adding JavaScript to the <code>head</code> of a document and not in the <code>body</code>?
* How can you benefit from your browser’s caching and what do you need to do to make it work for you?
* As search engines give the title of a document much love, wouldn’t it be useful to cram it full of relevant keywords? What are the downsides of this practice?
* As the title display can be a bit boring, wouldn’t it make sense to bold some words with a <code>b</code> element? Is that possible?
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}