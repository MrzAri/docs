{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199777 CSS Namespaces Module], Section 3


===Members===
The '''CSSNamespaceRule''' object has these types of members:
*[#properties Properties]


====Properties====
The '''CSSNamespaceRule''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/cssom/styleSheet/cssText|'''cssText''']]
|Sets or retrieves the persisted representation of the style rule.
|-
|'''namespaceURI'''
|Retrieves the namespace of the [[css/atrules/@namespace|'''@namespace''']] rule.
|-
|[[css/cssom/CSSRule/parentRule|'''parentRule''']]
|Retrieves the containing rule, if the current rule is contained inside another rule.
|-
|[[css/cssom/CSSRule/parentStyleSheet|'''parentStyleSheet''']]
|Retrieves the style sheet that contains the current rule.
|-
|'''prefix'''
|Retrieves the prefix of the @namespace rule or <code>null</code> if there is no prefix.
|-
|[[css/cssom/CSSRule/type|'''type''']]
|Retrieves the type of the rule.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>IHTMLCSSNamespaceRule</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}