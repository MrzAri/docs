{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the root node of the document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=documentElement
|Javascript_data_type=DOM Node
|Return_value_description=The root element of the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''documentElement''' property to get the [[dom/HTMLElement/innerHTML|'''innerHTML''']] property of the entire document.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function getHTML() {
   var sData {{=}} document.documentElement.innerHTML;
   document.getElementById("oResults").value {{=}} sData;
}
window.addEventListener("load", getHTML, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;textarea id{{=}}"oResults" cols{{=}}"50" rows{{=}}"10"&gt;&lt;/textarea&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=The root node of a typical HTML document is the '''html''' object.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}