Getting Started
===============

This page will guide you the basics of using pandoc with our template.

The usage is not diferent than any other pandoc command, the reason is
that the template provided works as a default template for any pdf conversion
using latex.

The full list of commands may be found here_

.. _here: http://pandoc.org/README.html

All the following examples will assume you have a file named test.md in the working directory

Creating a PDF
--------------

To create a PDF, simple type the following in your terminal
::
    pandoc test.md -o test.pdf

This command will use the template and create a PDF called test.pdf based on the test.md file (Markdown)

Or if you're using rst:
::
    pandoc test.rst -o test.pdf
    
This command will use the template and create a PDF called test.pdf based on the test.rst file (reStructuredText)

Creating the front page
-----------------------

We provide a simple yet powerful way to create the front page for your documents.

To do such, you just need to add pandoc's YAML meta data on the document's heading (before any other text)
for example, a document with the following data:
::
    ---
    title: Pràctica 0 - Teoria De Circuits
    subtitle: Mesures al Laboratori
    author:
     - Èrik Campobadal
     - Roger Solans
     - Aleix Gil
    ---

This will create a simple front page for your document, and clear the page after it.

At the same time, the page will not contain any number and will not be counted towards
page numering.

**NOTE** You can create another file called meta.yaml and place the yaml data there and then call it when converting:
::
    pandoc test.md meta.yaml -o test.pdf

**WARNING** Pandoc YAML metadata is only available in markdown (.md), if you use other markups such as **.rst** you'll need to provide
the information in the command line

Example:
::
    pandoc test.rst -o test.pdf -V title:'My Project Title' -V subtitle:'My Custom Subtitle' -V toc:true -V autodate:true

Front Page Logo
---------------

To se the front page logo you can use the following meta data:
::
    logo: true
    
To define a custom logo simply add the image to the images folder in your data directory (in my example):
::
    /home/erik/.pandoc/images

Add the images to that path and then you can get them the following way (example image: test.png in my images folder on my data dir):
::
    logo-image: test
    logo-height: 2
    logo-width: 2
    
The image height / width is set in **cm**

The image extension (.png) is ommited, you can google the supported image types for LaTeX)


Creating a Table Of Contents
----------------------------

To create a table of contents you'll just need to provide an extra meta data:
::
    toc: true
    toc-title: Contents
    toc-depth: 3
    numbersections: true

You can optionaly choose if you would like to change the default title, by default it's: Continguts

You can optionaly choose if you would like them to have a number.

The toc-depth specifies the level of section to include in table of contents

    
Additional Meta Data
--------------------

Some additional data you might use in your documents:

**Dates**

You can include the date in your front page with the following meta data:
::

    date: false
    autodate: true

You can also set an autodate variable to set the day at the day the document it's compiled (recommended)


**Abstract**

You can include an abstract in your document, that will be placed in the front page
::

    abstract: This is my abstract

**Includes**

You can handle the includes in the following way:
::
    include-before: Contents included before body (may have multiple values)
    include-after: Contents included after body (may have multiple values)
    
Other LaTeX Variables
---------------------

**papersize**

  paper size, e.g. letter, A4


**fontsize**

  font size for body text (e.g. 10pt, 12pt)


**documentclass**

  document class, e.g. article, report, book, memoir


**classoption**

  option for document class, e.g. oneside; may be repeated for multiple options


**geometry**

  option for geometry package, e.g. margin=1in; may be repeated for multiple options


**margin-left, margin-right, margin-top, margin-bottom**

  sets margins, if geometry is not used (otherwise geometry overrides these)


**linestretch**
  
  adjusts line spacing using the setspace package, e.g. 1.25, 1.5


**fontfamily**

  font package for use with pdflatex: TeX Live includes many options, documented in the LaTeX Font Catalogue. The default is Latin Modern.


**fontfamilyoptions**
  
  options for package used as fontfamily: e.g. osf,sc with fontfamily set to mathpazo provides Palatino with old-style figures and true small caps; may be repeated for multiple options


**mainfont, sansfont, monofont, mathfont, CJKmainfont**
  
  font families for use with xelatex or lualatex: take the name of any system font, using the fontspec package. Note that if CJKmainfont is used, the xecjk package must be available.


**mainfontoptions, sansfontoptions, monofontoptions, mathfontoptions, CJKoptions**

  options to use with mainfont, sansfont, monofont, mathfont, CJKmainfont in xelatex and lualatex. Allow for any choices available through fontspec, such as the OpenType features Numbers=OldStyle,Numbers=Proportional. May be repeated for multiple options.


**fontenc**

  allows font encoding to be specified through fontenc package (with pdflatex); default is T1 (see guide to LaTeX font encodings)


**colorlinks**
  
  add color to link text; automatically enabled if any of linkcolor, citecolor, urlcolor, or toccolor are set


**linkcolor, citecolor, urlcolor, toccolor**

  color for internal links, citation links, external links, and links in table of contents: uses any of the predefined LaTeX colors


**links-as-notes**
  
  causes links to be printed as footnotes


**indent**

  uses document class settings for indentation (the default LaTeX template otherwise removes indentation and adds space between paragraphs)


**subparagraph**

  disables default behavior of LaTeX template that redefines (sub)paragraphs as sections, changing the appearance of nested headings in some classes


**thanks**

  specifies contents of acknowledgments footnote after document title.


**toc**
  
  include table of contents (can also be set using --toc/--table-of-contents)


**toc-depth**

  level of section to include in table of contents


**lof, lot**

  include list of figures, list of tables


**bibliography**

  bibliography to use for resolving references


**biblio-style**

  bibliography style, when used with --natbib and --biblatex.


**biblatexoptions**

  list of options for biblatex.
