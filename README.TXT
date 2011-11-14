KindlePDFViewer
===============

This is a PDF viewer application, created for usage on the Kindle e-ink reader.
It is currently restricted to 4bpp inverse grayscale displays. It's using the
muPDF library (see http://mupdf.com/) and its UI is scripted using Lua (see
http://www.lua.org/).

The application is licensed under the GPLv3 (see COPYING file).


Building
========

Follow these steps:

- install muPDF sources into subfolder "mupdf"
- install muPDF third-party sources (see muPDF homepage) into a new subfolder
  "mupdf/thirdparty"

- install Lua sources into subfolder "lua"

=> note that there's a make target to do this. You need wget, unzip and git
   installed. Then just run "make fetchthirdparty".

- adapt Makefile to your needs

- run "make thirdparty". This will build MuPDF (plus the libraries it depends
  on) and Lua.

- run "make". This will build the kpdfview application


Running
=======

The user interface (or what's there yet) is scripted in Lua. See "reader.lua".
It uses the Linux feature to run scripts by using a corresponding line at its
start.
So you might just call that script. Note that the script and the kpdfview
binary currently must be in the same directory.
You would then just call reader.lua, giving the document file path as its first
argument.
