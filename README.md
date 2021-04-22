# Neon modules
This is a repository for various Neon modules and library code.

## xml.neon
This is an XML library for the [Neon](https://github.com/ghewgill/neon-lang) programming lanmguage.

#### Prerequisites
You need to have Neon compiled and functional.  Then place xml.neon into your `lib/` folder.  You can compile it with:
`bin/neonc lib/xml.neon`

#### Documentation
--ToDo: Create documentation for the XML library

#### DOM
ToDo: Describe the Document Object Model here.
All XML Documents start off from a `Document`, which contains a single member, `root`.  This is the root `Node` of your entire XML document.  
- Create a document from a string:
```Neon
IMPORT xml

LET xmlTest: String := @@"
<XMLDocument>
  <Node attribute1="attrVal">
    <ChildNode>Node Text</ChildNode>
  </Node>
</XMLDocument>
"@@
LET doc: xml.Document := xml.Parse(xmlText)
print(doc.toString())
```
- Load an XML file from disk:
```Neon
IMPORT xml

LET doc: xml.Document := xml.loadFromFile("xmldata.xml")
print(doc.toString())
```
