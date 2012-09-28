{{Page_Title}}
{{Flags}}
{{Summary_Section|This article shows how to use JavaScript to modify the CSS applied to an HTML page, and create new styles.}}
{{Guide
|Content=== Introduction ==
 
At this point in the JavaScript section of the [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum], you’ve already covered the real basics of JavaScript usage, looked at how to target elements using the DOM, and seen how to manipulate them once you’ve successfully targeted them.
 
In this article we will look at how to dynamically update the styling applied to your elements by manipulating your CSS at runtime using JavaScript. It uses the same kind of technique that we’ve already seen, but there are a few special considerations to keep in mind when ''working with the CSS DOM''.
 
== Accessing style sheets ==
 
The browser provides an interface to interact with style sheets — in your JavaScript code you can access a list of your style sheets by using <code>document.styleSheets</code>. <code>document.styleSheets</code> will return a list of all of the style sheets applied to a page, including external style sheets referenced with a <code>link</code> element and internal style sheets residing inside <code>style</code> elements. If your <code>style</code> elements have <code>id</code> attributes, you can reference them quickly with <code>document.getElementById(''element_id'')</code>.
 
You can also add new style sheets to the page — you can use the <code>document.createElement</code> function to create a new <code>style</code> element. This is useful when you want to give site visitors the option of changing your site styles dynamically, using some button controls perhaps. Here is a quick example of how you could create a new style sheet:

<pre>var sheet = document.createElement('style')
sheet.innerHTML = "div {border: 2px solid black; background-color: blue;}";
document.body.appendChild(sheet);</pre>
 
Removing a style sheet is also very simple. First you must obtain the style sheet you wish to remove. You can do this by using <code>document.getElementById</code>, as shown in the small example below. To remove a style sheet you can use the DOM function <code>''parent''.removeChild(''element'')</code>, where <code>element</code> is the style sheet object you wish to remove and <code>parent</code> is the parent node of our style sheet. As shown in the example below, to remove the style sheet (<code>sheetToBeRemoved</code>) you first get the style sheet's parent — <code>var sheetParent = sheetToBeRemoved.parentNode</code> — then you call <code>removeChild</code> with an argument of <code>sheetToBeRemoved</code> - <code>sheetParent.removeChild(sheetToBeRemoved)</code>

<pre>var sheetToBeRemoved = document.getElementById('styleSheetId');
var sheetParent = sheetToBeRemoved.parentNode;
sheetParent.removeChild(sheetToBeRemoved);</pre>
 
The [http://dev.opera.com/articles/view/dynamic-style-css-javascript/accessingstylesheets.html accessing style sheets example] demonstrates both accessing all styles sheets and adding and removing a new style sheet to the page.

== Style Sheet Properties ==
 
The <code>stylesheet</code> object is available through JavaScript, and allows you to access information about a style sheet referenced from the current web page, such as if it is disabled, its location, and the list of CSS rules it contains. For a full list of the properties of the <code>stylesheet</code> object (and many things besides), check out the [http://www.w3.org/TR/DOM-Level-2-Style/stylesheets.html W3C Document Object Model Style Sheets documentation].
 
Let’s consider a (currently) theoretical example — say we have a website where we show a series of technical articles. We want to spotlight some of these articles in a nice animated carousel, but what about users that don’t have JavaScript enabled for whatever reason? Thinking back to our [http://www.w3.org/wiki/The_principles_of_unobtrusive_JavaScript unobtrusive JavaScript knowledge], we want the website functionality to still work for these users, but we might want to style the site differently for those users so that their user experience is still pleasant, even without the carousel.
 
What you want is a style sheet that gets enabled only if JavaScript is enabled. You are in luck — the DOM style sheet interface gives us access to the <code>disabled</code> attribute, which allows us to turn style sheets on or off.
 
Most of the properties of the <code>stylesheet</code> object are read only, but some, such as <code>disabled</code>, aren’t.
 
You can also use the style sheet properties to help differentiate between multiple style sheets on the page. The <code>src</code> property can help you identify external style sheets, but it won’t help you to reference internal style elements. A better way, which allows you to reference both internal and external style sheets individually, is to use the <code>title</code> property. If you iterate through <code>document.styleSheets</code> you can differentiate between the different style sheets you have included on the page. The following example shows how you can accomplish this iteration:
 
<pre>function getStyleSheet(unique_title) {
  for(var i=0; i&lt;document.styleSheets.length; i++) {
    var sheet = document.styleSheets[i];
    if(sheet.title == unique_title) {
      return sheet;
    }
  }
}</pre>
 
For each <code>stylesheet</code> object retrieved from the <code>styleSheets</code> array you can access its <code>title</code> property to check if it has the title our code is looking for. You can see a functional example of this in the [http://dev.opera.com/articles/view/dynamic-style-css-javascript/addingandremovingrules.html adding and removing rules example], which I will discuss in the next section.

Switching between different style sheets based on user preference is a fairly common web site feature — using what we have discussed so far, you can set up multiple style sheets and enable only the ones that the current site visitor would want to view. Let’s look at a real example — initially the text is styled, but when we set the <code>disabled</code> attribute to <code>true</code>, our defined CSS gets disabled. You can easily turn the CSS back on by setting <code>disabled</code> to <code>false</code>. Check out my [http://dev.opera.com/articles/view/dynamic-style-css-javascript/stylesheetproperties.html style sheet properties example] for a practical look at how to use this.

== Adding and Removing Rules ==
 
Remember the theoretical showcase site we discussed above? Let’s say this site has a list of articles; some are about CSS, some are about HTML, and some are about JavaScript. On our webpage we show all the articles at once, but our user only wants to see the CSS articles. How might we do this? Because all the articles are already being shown, we don’t want to do another round trip to the server to get to a page containing just the CSS articles — that is a waste of time.
 
To solve this issue, we can use JavaScript to either iterate through all the articles and only make the CSS articles visible (I’ll discuss how to do this later), or add a rule to one of our style sheets that will make only the CSS articles visible. Using CSS will actually be faster than traversing over all the elements.
 
Our <code>stylesheet</code> object has two functions to help us with this problem. First is the <code>insertRule</code> function, which looks like this:
 
<pre>stylesheet.insertRule(rule,index)</pre>
 
<code>rule</code> is a string containing the rule we would like to add to the style sheet. <code>index</code> specifies where within the style sheet’s rule list the rule should be placed. Here is how it might look.

<pre>stylesheet.insertRule(".have-border { border: 1px solid black;}", 0);</pre>
 
I’ve created an example to demonstrate how the <code>insertRule</code> function is used. In this example is a list of all the rules in a style sheet. When the button is pressed it adds a rule with an index of 2 to make the text red by adding the property <code>color: red</code> to the <code>p { ... }</code> rule. Take a look at the [http://dev.opera.com/articles/view/dynamic-style-css-javascript/addingandremovingrules.html adding and removing rules example].

If you want to delete this rule, you can call the function <code>stylesheet.deleteRule(index)</code>, where <code>index</code> is the index of the rule you want to be removed.
 
In our article showcase example, we can create a rule that turns the display to <code>none</code> for all the HTML and JavaScript articles — check out the [http://dev.opera.com/articles/view/dynamic-style-css-javascript/carousel.html carousel example] to see this in action.
 
Note: IE does not implement rules according to the standard. Instead of the attribute <code>cssRules</code> it uses <code>rules</code>. IE also uses <code>removeRule</code> instead of <code>deleteRule</code> and <code>addRule(selector, rule, index)</code> instead of <code>insertRule</code>.

== Changing Element Styles ==
 
At this point you should understand how to edit style sheets connected to the page and create and modify the CSS rules within them. What if you want to change a specific element inside the DOM? Using the DOM API you can access the specific elements of your page. Looking back at our [http://dev.opera.com/articles/view/dynamic-style-css-javascript/carousel.html carousel example], functionality is defined so that when you click on an article, that article becomes highlighted while the main article text gets displayed below.
 
Through the DOM, you have access to a <code>style</code> object that describes the style of an element. This <code>style</code> object is defined as a ''CSSStyleDeclaration''; you can see a detailed explanation of this at the [http://www.w3.org/TR/DOM-Level-2-Style/css.html#CSS-CSSStyleDeclaration W3C documentation of the CSSStyleDeclaration interface]. The <code>style</code> object doesn’t quite work the same as some of the other properties defined in your HTML element. Unlike <code>element.href</code> or <code>element.id</code>, which return strings, <code>element.style</code> returns an object. This means you cannot set the style by assigning a string to <code>element.style</code>.
 
The <code>style</code> object has attributes that correspond to the different CSS properties we set. For example, <code>style.color</code> returns the colour that element has set on it. By calling <code>element.style.color = "red";</code> you can apply the style change dynamically. Below is a function that turns an element’s colour to red when you pass it the element’s <code>id</code>.
 
<pre>function colorElementRed(id) {
  var el = document.getElementById(id);
  el.style.color = "red";
}</pre>
 
You could also use <code>setAttribute(key, value)</code> to set a style on an element. For example, you could set the colour of an element to red by calling <code>element.setAttribute('style', 'color: red');</code> on the element, but be wary as this ''will'' erase any changes you have made to the <code>style</code> object.

When you set the style of an element in this manner it is the same as if you were assigning it as a declaration in a <code>style</code> attribute of the <code>html</code> element. The style will only be applied if the importance and specificity of the rule is greater than the other rules applied to the element (specificity is explained in the article about [http://www.w3.org/wiki/Inheritance_and_cascade the inheritance and cascade of CSS].
 
Some of you may be wondering what happens when the CSS property being set has a hyphen. The syntax has to be different here, because for example if you write <code>element.style.font-size</code>, JavaScript will try to subtract <code>size</code> from the <code>element.style.font</code> notation, which is not what you want to happen. To stop this problem from occurring, all the CSS properties are written out in '''CamelCase'''. As shown below, you should write <code>element.style.fontSize</code> to access the element’s font size. For example:
 
<pre>function changeElement(id) {
  var el = document.getElementById(id);
  el.style.color = "red";
  el.style.fontSize = "15px";
  el.style.backgroundColor = "#FFFFFF";
}</pre>
 
Remember those stylesheet objects? Well, <code>styleSheet.cssRules</code> will return a list of <code>style</code> objects representing all the CSS rules contained in the style sheet. You can use these <code>style</code> objects just like the <code>style</code> objects for the other elements. In this case, rather than changing one specific element on our page, changes here will change all elements that the CSS rules apply to.

In the example below, the function to make the text bigger uses the <code>style</code> object and the function to make it smaller uses <code>setAttribute</code>. If you set the text to red and then call <code>setAttribute</code> with the smaller text button, you will notice that our change gets overwritten. Check out the [http://dev.opera.com/articles/view/dynamic-style-css-javascript/changingelementstyles.html changing element styles example] live.

== Element Class Names ==
 
Another way to alter the style of an element is by changing its <code>class</code> attribute. <code>class</code> is a reserved word in JavaScript, so in order to access the element’s class, you use <code>element.className</code>. You can append strings to <code>className</code> if you want to add a class to an element, or you could just overwrite <code>className</code> and assign it a whole new class. Check out the [http://dev.opera.com/articles/view/dynamic-style-css-javascript/elementclassnames.html element class names example].
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections==== Exercise Questions ===
 
* What is the difference between <code>setAttribute</code> and setting the style through the ''CSSStyleDeclaration'' object?
* List two ways that you could cause all images to have a green border when a user clicks a button.
* Will changing the ''CSSStyleDeclaration'' object of an element always change the element’s style?  Why?
* List two ways to access a specific style sheet.
}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}