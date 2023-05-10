{{{m1}}}
[[
Welcome
-------
This is a template called markdown.md. 
 
It is a simple text document with certain words or phrases tagged, so that it can be regenerated into an html page.

Files must on a server (with a url) or within the /files folder of this extension.


Files can be edited in the app and then saved. No need to write HTML.

![Jigsaw](https://res.cloudinary.com/geocloud/image/upload/v1683148390/world-habitat-day-close-up-picture-piece-white-jigsaw-each-hand_poxzet.jpg)

]]
{{m2}}
[[
Markdown
--------

Markdown is a way to create simple text files and enable them to be converted into HTML for viewing purposes. Any text editor can be used. 
Alternatively the in app editor can be used.

These are some examples:

Horizontal lines
================

___ (3 x underlines with breaks above and below)

will render as

___

Header 1
--------

Header text
₋₋₋₋₋₋₋₋₋₋₋₋₋₋₋ 

will render as ...

Header text
-----------

___

Header 2
========

Header text
⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼⁼ 

will render as ...

Header text
===========

___

Links
=====

&#x5b;title ] ( url )

Example

&#x5b; Password Guidelines ] ( https://design-system.service.gov.uk/patterns/passwords/ ) 

will render as ...

[Password Guidelines](https://design-system.service.gov.uk/patterns/passwords/).

___

Images
======

! &#x5b; title ] ( url )

Example

! &#x5b; Jigsaw ] ( https://res.cloudinary.com/geocloud/image/upload/v1683148390/world-habitat-day-close-up-picture-piece-white-jigsaw-each-hand_poxzet.jpg ) 

will render as ...

![Jigsaw](https://res.cloudinary.com/geocloud/image/upload/v1683148390/world-habitat-day-close-up-picture-piece-white-jigsaw-each-hand_poxzet.jpg)

Unordered lists
===============

∗apples
∗pears
∗strawberries
∗lemons

renders as

*apples
*pears
*strawberries
*lemons


Ordered lists
===============

1. apples
2. pears
4. strawberries
3. lemons


Quotes
===============

&#62; Once upon a time ...

renders as

> Once upon a time ...


Underline
=========

(x3 _ before and after the text)

̲ ̲ ̲ apples ̲ ̲ ̲ 

renders as
___apples___


Strike through
==============

̴ ̴  text to be deleted   ̴ ̴

~~text to be deleted~~


Bold
====
⁎⁎ bold ⁎⁎

**bold**

_italics_


Monospace / Code
================

&grave; this is monospace code &grave;

renders as

`this is monospace code`

Quote
=====
: " dasdasd " :

:"This is a quote":


]]

{{m3}}
[[
How to create a group
---------------------

Grouping text together and giving them an index id. 

In the text file, wrap groups like this:
{ { menu id } }
[ [ lots of text ] ]



]]

{{m4}}
[[
Working with files
---------------------

There are 2 files required.

1. a menu file in CSV format
2. a markdown text file

If the markdown is sensitive, it should be edited in Settings and 
* the encrypted check box checked 
* a password entered

before saving the markdown file (menus cannot at present be encrypted). The file will be encrypted and encoded into base64. Unless they password is known and the cryptographic algorithm used, the file will be useless to a bad actor.

Note the password needs to present in Settings at all times. If the browser cache is hard deleted, you should check the password has not been deleted.

menu file
=========
This is a csv (comma sepeareted values) file with 3 parts [index],[title],[type].
No header is required although can be put in.

**Example**

menu id, title, type
menu1,Welcome,orphan
menu2,How it works,parent
menu3,Starting, child
menu4,Finishing, child
menu5, Closing thoughts,orphan

The [index] is used to open the group of text in the markdown file.
The title is the title of the menu option.
The type is orphan ; parent ; child.

This is saved as [filename].csv

]]