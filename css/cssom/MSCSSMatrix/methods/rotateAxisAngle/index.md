{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return value
!Description
|-
|S_OK
|The operation completed successfully.
|}
 

MSCSSMatrix

The returned matrix.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 10.1


===Parameters===
;''x'' [in]:Type: '''float'''The ''x'' component of the axis vector.
;''y'' [in]:Type: '''float'''The ''y'' component of the axis vector.
;''z'' [in]:Type: '''float'''The ''z'' component of the axis vector.
;''angle'' [in]:Type: '''float'''The angle (in degrees) of the rotation about the axis vector.
;''retMatrix'' [out, retval]:Type: '''MSCSSMatrix'''The returned matrix.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/transforms/MSCSSMatrix|MSCSSMatrix]]</code>
|Topic_clusters=Transforms
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}