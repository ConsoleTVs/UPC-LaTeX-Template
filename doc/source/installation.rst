Installation
============

Installing the templates takes only a few steps, you can use the template in diferent
ways, but we'll show how to add it as the default pandoc template

Prerequisites
-------------

You'll need to have pandoc installed (linux - Debian / Ubuntu):

To use the full features of pandoc, please install the version 1.16, not the 1.12 that comes with ubuntu

- **RECOMMENDED** Version 1.17:

  `Download 1.17`_

  .. _`Download 1.17`: https://github.com/jgm/pandoc/releases/download/1.17.2/pandoc-1.17.2-1-amd64.deb

- **NOT RECOMMENDED** Version 1.12:
  ::
      sudo apt-get install pandoc

Download for Windows_

.. _Windows: https://github.com/jgm/pandoc/releases/download/1.17.2/pandoc-1.17.2-windows.msi

You'll also need to install LaTeX (linux - Debian / Ubuntu):
::
    sudo apt-get install texlive
    
For other operating systems, please take a closer look at pandoc installation page:

http://pandoc.org/installing.html


Downloading
-----------
To install our template you'll need to download the files first:

Version: **1.6**

Download_

.. _download: https://www.dropbox.com/s/3kqk92ijs4e2mzc/UPC.tar.gz?dl=1

Installing
----------

Once the file has been downloaded you'll need to place the files under the pandoc
default folder.

To see where the folder is located, you can type the following in your terminal:
::
    pandoc -v
    
This will give you a list of information about pandoc, you just need to get the default folder location, here's an example output:
::
    Default user data directory: /home/erik/.pandoc
    
You will then need to place the files provided in the download section in your home folder, creating the .pandoc folder if it did not exist.

The template file should then be available under the following location (example):
::
    /home/erik/.pandoc/templates/default.latex
    
If everything went well you should then have the template installed and ready to go, take a look at the getting started page to learn how to use it.

Updating
--------

To update the template, simply run the python script in the .pandoc folder like follows:

**Note:** Python 2.7 Required
::
  python update.py
