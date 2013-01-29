Vusion Documentation
This documentation is covering the use of Vusion.

Requirements
You can read all of the documentation within as its just in plain text files, marked up with ReST text formatting. To build the documentation you'll need the following:

Make
Python
Sphinx
PhpDomain for sphinx
You can install sphinx using:

easy_install sphinx
You can install the phpdomain using:

easy_install sphinxcontrib-phpdomain
Building the documentation
After installing the require packages you can build the documentation using Make

# Create all the HTML docs. Including all the languages.
make html

# Create just the english HTML docs.
make html-en

# Create all the EPUB (e-book) docs.
make epub

# Create just the engish EPUB docs.
make epub-en

# Populate the search index
make populate-index
This will generate all the documentation in an html form. Other output such as 'pdf' and 'htmlhelp' are not fully complete at this time.

After making changes to the documentation, you can build the html version of the docs by using make html again. This will build only the html files that have had changes made to them.
