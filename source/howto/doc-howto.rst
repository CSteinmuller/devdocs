Introduction
####################

12 Febuary 2018, 18:32 GMT

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
of columns the title has, plus eight. The date 
also appears only once in the file and appears 
below the first title.

Subsection: Every subsection must look like this:

..  code-block:: rst

  Subsection
  ==============================

where the subsection title's first letter is capitalized 
and the equal signs "=" always amount to 30 columns.

Sub-subsection: A sub-subsection looks like this:

..  code-block:: rst

    Sub-subsection
    ----------------

where the subsection title's first letter is capitalized
and the amount of dashes is entirely due to the writer's
preferences.

Date: Formatted as: dd mm yyyy, hh:mm GMT

Description: The description's amount of columns can
be unlimited; however, one line *must* never consist
of two lines (If you have text wrapping disabled, you
can easily notice this situation).


Miscellaneous
==============================

For more information on RST formatting, check 
`RST http://www.sphinx-doc.org/en/stable/rest.html`_.
