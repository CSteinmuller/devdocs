Documentation Howto
###########################

24 Febuary 2018, 18:32 GMT

This file is targeted at people who want
to document the project but don't know what
guidelines to follow.


Writing a New File
==============================

If creating a new documentation file, it must
include the following:

Introduction: Succinct description about
what the file is dedicated to.

Date: Include the date it was created after
the Introduction title.

Description: Long description about the subject;
it must be very clear, readable and free of
grammatical and spelling errors.


The file must be in RST format. However, if you're making a
.md file, it must be outside the source/ directory.

When you successfully create an RST file, put this file
in the Table of Contents section of source/index.rst.
When inserting a file in the index.rst file, do not
insert a file extension at the end of the filename.
Another rule when putting the file in the Table of
Contents section of the index.rst file, it must have
the path to the file that amount to one line. An example
is shown below as to what it should look like in the index.rst
file.

..  code-block:: rst

    howto/doc-howto
    howto/gettingstarted
    serverconfig/config

Note that the source/ directory isn't seen here. That is because,
to Sphinx, everything inside the source/ directory is considered;
whereas, Sphinx is blind to everything else outside the source/
directory other than make-related files such as Makefile. The order
of files in the Table of Contents must be alphabetical.


Format Standards
==============================


RST format
-----------

If writing documentation in a ".rst" file,
the following format standards are:

Title: The format is:

..  code-block:: rst

    Title/Section
    #####################

    Date

Capitalize the major words of the title/section
and the pounds "#" should always be the amount
of columns the title has, plus eight. The title
must appear only once in the file, and it must
appear at the very top. The date also appears
only once in the file and appears below
the first title.

Subsection: Every subsection must look like this:

..  code-block:: rst

  Subsection
  ==============================

Where the subsection title's first letter is capitalized
and the equal signs "=" always amount to 30 columns. The
only exception is if the subsection title is longer than
30 columns. If this is the case, only amount an equal sign
"=" to the amount of characters the title has, plus one.

Sub-subsection: A sub-subsection looks like this:

..  code-block:: rst

    Sub-subsection
    ------------------

Where the subsection title's first letter is capitalized
and the amount of dashes is entirely due to the writer's
preferences as long as it is longer than the sub-subsection's
title text.

Date: Formatted as: dd mm yyyy, hh:mm GMT

Description: The description's amount of columns can
be unlimited; however, one line *must* never consist
of two lines (If you have text wrapping disabled, you
can easily notice this situation).

Syntax: Titles/subsections/sub-subsections must be separated
from each other by two spaces.

Links: Links should only be shown as hyperlinks, *never* as
raw links. As an example, https://qub3d.org needs to be given
the name, "Qub3d." A way to do this is demonstrated in the following:

..  code-block:: rst

    https://qub3d.org

This should never be shown by itself. Instead, it should be displayed
like this:

..  code-block:: rst

    `Qub3d https://qub3d.org`_

This shows "Qub3d" as a hyperlink for qub3d.org.


MD Format
----------

It is rare to write .md files other than the README
and the LICENSE. However, there can be a time where a .md file
gets written. If that's the case, then the following format standards
are required to write a .md file for the Qub3d project. They are:

Title: It must be formatted as:

..  code-block:: markdown

    # Title

Where the first letter is capitalized and there is only one
pound "#" before the title.

Subsection: It must be formatted as:

..  code-block:: markdown

    ## Subsection About Stuff

Where the subsection always comes after the Title, and all major
words are capitalized. Subsections also must be consistent with
two pounds "##" before the subsection title.

Date: See RST Format's Date section.

Description: The amount of columns are limited to 60. If you're
starting a new subject within the same section, you must have a
space between the two subjects. When doing bullet/list points,
you must insert a plain text description between the title and
the list/bullet points.

Links: Never put in raw links. Instead, give these links a name.
For example, the file shouldn't display https://qub3d.org by itself.
Instead it should be given the name, "Qub3d." This is demonstrated in
the following:

..  code-block:: markdown

    https://qub3d.org

This is incorrect. What should've been done is:

..  code-block:: markdown

    [Qub3d](https://qub3d.org)

This displays "Qub3d" as a hyperlink to qub3d.org.


Miscellaneous
==============================

For more information on RST formatting, check
`RST <`http://www.sphinx-doc.org/en/stable/rest.html>`_.

NOTE: This file is *not* a tutorial on RST and MD, rather, it is a
tutorial on RST and MD standards used by the Qub3d Engine Group.
