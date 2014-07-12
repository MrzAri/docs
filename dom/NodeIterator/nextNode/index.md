{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set.  The first call to nextNode() returns the first node in the set.

This method returns null when there are no nodes left in the set.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oNode
|Data type=any
|Description=Object containing
the next node in the list.
|Optional=No
}}
|Method_applies_to=dom/NodeIterator
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}InvalidStateError _ERR
{{!}}NodeIterator raises this exception if detach has been invoked on the object.
{{!}}}
 

[[dom/Node|'''Node''']]

Object containing
the next node in the list.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;NextNode example&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;
    function LoseMondays(){
	  var ni {{=}} document.createNodeIterator(document.body, NodeFilter.SHOW_TEXT, null, false);
      var txt {{=}} ni.nextNode();      //go to first node of our NodeIterator
      while (txt)                   //while text
        {
          if (txt.wholeText.match('Monday') {{!}}{{!}} txt.parentNode.getAttribute('id') {{=}}{{=}} 'Monday')
            {
            txt.parentNode.removeChild(txt);        //remove monday's activity
            }
          txt{{=}}ni.nextNode();                        //go to next node
        }
    }
    function refresh()                 
      {
        window.location.reload( false );           //reload our page
      }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;&lt;strong&gt;Harry's weekly diary&lt;/strong&gt;&lt;/p&gt;
    &lt;p&gt;Monday Joe bought a turkey.&lt;/p&gt;
    &lt;p&gt;Tuesday Bill bought a pound of ham.&lt;/p&gt;
    &lt;div&gt;Chuck called in sick Monday.&lt;/div&gt;
    &lt;p id{{=}}"Monday"&gt;CALL supplier today&lt;/p&gt;
    &lt;p&gt;Wednesday's delivery was delayed.&lt;/p&gt;
    &lt;input type{{=}}"button" name{{=}}"reset" value{{=}}"refresh" onclick{{=}}"refresh()"/&gt;
    &lt;input type{{=}}"button" name{{=}}"cutmonday" value{{=}}"Lose Mondays" onclick{{=}}"LoseMondays()"/&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This example shows how to create a [[dom/NodeIterator|'''NodeIterator''']] and move forward through the list of nodes.
|Import_Notes====Syntax===
node {{=}} nodeIterator.nextNode();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-nodeiterator-nextnode
|Status=Living Standard
|Relevant_changes=As detach() is now a no-op method, this method cannot throw anymore.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.nextNode NodeIterator.nextNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975281(v=vs.85).aspx nextNode Method]
|HTML5Rocks_link=
}}