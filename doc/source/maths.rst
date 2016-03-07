Mathematics
===========

You can create Mathematical formulas and operations using Pandoc, to do such simple type the formula like this:
::
  $(a + b)$

You'll need to phrase all the mathematical formulas leaving a blank space on the left before the first $ and
a blank space on the right in the last $

This will be translated into a mathematical formula once the conversation has been done.

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

