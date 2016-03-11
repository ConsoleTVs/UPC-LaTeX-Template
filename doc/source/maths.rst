Mathematics
===========

You can use diferent maths operations with pandoc, here you might get the idea of how they are done

For more information, check Maths_

.. _Maths: http://pandoc.org/README.html#math

Markdown, LaTeX, Emacs Org mode, ConTeXt
----------------------------------------

You can create Mathematical formulas and operations using Pandoc, to do such simple type the formula like this:
::
  $(a + b)$

You'll need to phrase all the mathematical formulas leaving a blank space on the left before the first $ and
a blank space on the right in the last $

You can of course, use signs and other variables, to do such, simply take a look at this_ PDF, it contain a list of usefull
signs that can be used inside the $ $

.. _this: ftp://ftp.ams.org/pub/tex/doc/amsmath/short-math-guide.pdf

Another source with usefull signs: Here_

.. _Here: http://web.ift.uib.no/Teori/KURS/WRK/TeX/symALL.html

A quick example:
::
  $3 \pi r$
  
Will be translated into 3PIr with the PI sign.

Another example:
::
  $\pi \cdot R^{2}$
  
This will be translated into PI * R^2

Better Usage
------------

The best way to use the formulas is the following:
::
  $$
  (a + b) \cdot \pi + \int_0^5{2x}
  $$
  
This will center the formula and at the same time make it in a new line, so it will have better space and will be better to look at.

reStructuredText
----------------

The syntax it's diferent, you can use:
::
  :math:`A_\text{c} = (\pi/4) d^2`.

This will create the correct maths text.

