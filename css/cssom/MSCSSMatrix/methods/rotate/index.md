{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Proprietary.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=/css/cssom/MSCSSMatrix
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
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 10.1


===Parameters===
;''angleX'' [in]:Type: '''float'''The angle (in degrees) of the rotation along the ''x''-axis. If ''angleY'' and ''angleZ'' are undefined, this method becomes a rotation ''angleX'' degrees around the ''z''-axis.
;''angleY'' [in, optional]:Type: '''float'''Angle (in degrees) of the rotation along the ''y''-axis.
;''angleZ'' [in, optional]:Type: '''float'''Angle (in degrees) of the rotation along the ''z''-axis.
;''retMatrix'' [out, retval]:Type: '''MSCSSMatrix'''The returned matrix.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>[[css/transforms/MSCSSMatrix|MSCSSMatrix]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}