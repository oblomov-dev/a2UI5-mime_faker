# a2UI5 - cloud mime fake dummy
This is not a mime repository!

Store your files in classes:
```abap
  METHOD z2ui5_if_mime_container~container.
*{
*    "glossary": {
*        "title": "example glossary",
*        "GlossDiv": {
*            "title": "S",
*            "GlossList": {
*                "GlossEntry": {
*                    "ID": "SGML",
*                    "SortAs": "SGML",
*                    "GlossTerm": "Standard Generalized Markup Language",
*                    "Acronym": "SGML",
*                    "Abbrev": "ISO 8879:1986",
*                    "GlossDef": {
*                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
*                        "GlossSeeAlso": ["GML", "XML"]
*                    },
*                    "GlossSee": "markup"
*                }
*            }
*        }
*    }
*}
 ENDMETHOD.
```
Use the interface:
```abap
INTERFACE z2ui5_if_mime_container
  PUBLIC.

  TYPES:
    BEGIN OF ty_s_metadata,
      name   TYPE string,
      format TYPE string,
      descr  TYPE string,
    END OF ty_s_metadata.

  METHODS get_metadata
    RETURNING
      VALUE(result) TYPE ty_s_metadata.

  "! Dummy Container, filled with file data as comments, don't use this!
  METHODS container.

ENDINTERFACE.
```

And check out your files with an abap2UI5 app:
<img width="600" alt="image" src="https://github.com/oblomov-dev/a2UI5_cloud_mime_fake/assets/102328295/cdd2a42a-a40a-4c01-b3de-64f1299c2f40">
# Demo