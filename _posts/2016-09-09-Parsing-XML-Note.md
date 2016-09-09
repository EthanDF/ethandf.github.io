---
layout: post
title: A Note on Parsing XML
---

Parsing XML is something I haven't had to do a lot of. I scrape web pages in HTML and usually extract the text I need. However, I know I'm going to need to get better at parsing XML.

Leaving this as a bread crumb to come back to later. It's from a Code Academy course on Using APIs with Python

```sh
from xml.dom import minidom

f = open('pets.txt', 'r')
pets = minidom.parseString(f.read())
f.close()

names = pets.getElementsByTagName('name')
for name in names:
	print name.firstChild.nodeValue
```

XML File

```sh
<pets>
  <pet>
    <name>Jeffrey</name>
    <species>Giraffe</species>
  </pet>
  <pet>
    <name>Gustav</name>
    <species>Dog</species>
  </pet>
  <pet>
    <name>Gregory</name>
    <species>Duck</species>
  </pet>
</pets>
```