Quick Guide
===========

Some quick guide to see how pandoc works under the markdown document

**NOTE:** This guide is written for markdown

Centering Text
--------------

To center some text, just type the following anywhere in your markdown code:
::
  \begin{center}
  Some centered text
  \end{center}

Images
------

To include images, use the following:
::
  ![Image](https://i.ytimg.com/vi/gxmHOwWh-i4/maxresdefault.jpg){width=50%}

This will include an image and use 50% of the document width (add a final \ to create an inline image)

Tables
------

Table generator site_

.. _site: http://www.tablesgenerator.com/markdown_tables

To create simple tables, simply use the following example:
::
  | Test Table     | This a test table | Some other field |
  |----------------|-------------------|------------------|
  | Random value   | Random value      | Random value     |
  | Some more text | Some more text    | Some more text   |
  

Bold & italic
-------------

- Bold
  ::
    **I'm bold**

- Italics
  ::
    *I'm italic*

Links
-----

To create simple liks (and make them clickable) just add the following:
::
  <http://google.com>

Another way is telling the link text:
::
  [This link](http://example.net/)
  
Lists
-----

To define lists, simply do the following:

- Bullet lists:
  ::
    - One
    - Two
- Numbered lists
  ::
    1. Number 1
    2. Number 2
    
Code Block
----------
  
To add a code block, simply type the code in the following way
::
  ```
  Code Here
  ```

If you need to syntax highlight it:
::
  ```python
  s = "Python syntax highlighting"
  print s
  ```
  
  ```Vhdl
  Vhdl code
  ```
