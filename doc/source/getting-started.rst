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
    
This command will use the template and create a PDF called test.pdf based on the test.md file

Creating the front page
-----------------------

We provide a simple yet powerful way to create the front page for your documents.

To do such, you just need to add pandoc's YAML meta data on the document's heading
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

Creating a Table Of Contents
----------------------------

To create a table of contents you'll just need to provide an extra meta data:
::
    toc: true
    numbersections: true

You can optionaly choose if you would like them to have a number.

Additional Meta Data
--------------------

Some additional data you might use in your documents:

**Dates**

You can include the date in your front page with the following meta data:
::

    date: false
    autodate: true

You can also set an autodate variable to set the day at the day the document it's compiled (recommended)

