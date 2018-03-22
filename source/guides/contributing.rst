Contributors' Guide
###########################

25 Febuary 2018, 05:27 GMT

This file is dedicated to people who want to
contribute to the project but don't know what
Qub³d Engine Group's guidelines are.

You want to contribute to the project? Awesome!
Here, you will find out how to get started.


Getting Started
==============================

This section displays the guidelines for making a development
environment for the Qub³d project.

Create an account on Qub³d Engine Group's `Phabricator <https://phab.qub3d.org>`_
using your GitHub account. If you don't have a GitHub
account, go ahead and create one. It's free, only takes
a couple minutes, and gives you access to the majority
of the open source development world! After you're done
creating one, on the main page, click on your profile
picture somewhere at the top right and click on :guilabel:`Settings`
and customize/configure to your heart's content.

Go to your Phabricator profile's home page by clicking on your
profile picture at the top right region, click on :guilabel:`Manage`. On the
right, you will see :guilabel:`Edit Profile`. Click on it and fill in the blanks
to your heart's content.

Before submitting contributions, the Qub³d Engine Group will need
verification that you have signed the `Terms of Development <https://phab.qub3d.org/L2>`_.


Development Environment
------------------------

Supported operating systems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Windows 7/8/8.1/10

- MacOS

- Any Linux distribution

- FreeBSD

Dependencies
^^^^^^^^^^^^^

- `Cinder <https://libcinder.org>`_

- `PawLIB <https://mousepawmedia.com/pawlib>`_

- `CMake <https://cmake.org/>`_

- `Sphinx <https://sphinx-doc.org>`_

Cinder is the library that the Qub³d engine requires
in order to work.

PawLIB is the library that Qub³d requires in order to
work. It has the Goldilocks testing suite
required by the Qub³d Engine Group.

CMake is the cross-platform compiling software that
most of the Qub³d Engine Group's repositories require.

Sphinx is the software used to make documentation
cleaner. It is required by the Qub³d Engine Group if
you're working on documentation or want to read the
documentation locally in a specified file format.


Installation of CMake
^^^^^^^^^^^^^^^^^^^^^^

For Windows, TO BE FILLED IN LATER

For MacOS, TO BE FILLED IN LATER

For Linux distributions with the Apt package manager, simply type:

..  code-block:: bash

    $ sudo apt-get install cmake

And it will do the magic for you. For Gentoo and its derivatives, type:

..  code-block:: bash

    $ sudo emerge -av dev-util/cmake

For Linux distributions with the DNF package manager, type:

..  code-block:: bash

    $ sudo dnf install cmake

If you have a Linux installation without a package manager like
(B)LFS, you can compile from source and install it. `The tarball
for CMake is here <https://cmake.org/download>`_.


FreeBSD
^^^^^^^^

Type:

..  code-block:: bash

    % sudo pkg install cmake


Installation of Cinder (UNIX only)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Clone the Cinder repository <https://github.com/cinder/Cinder>`_
 by typing:

..  code-block:: bash

    $ git clone https://github.com/cinder/Cinder cinder_master


Then, `cd` to cinder_master and run :code:`cmake . -DCINDER_BOOST_USE_SYSTEM=1`
in a user-created `build` directory.
Once that's done, run `make -j<number of enabled CPU threads>` to build.

NOTE: cinder_master *must* be in your home directory `/home/user/` and no other place.
It can't be in any other directory within the home directory.


Installation of PawLIB
^^^^^^^^^^^^^^^^^^^^^^^

`Install PawLIB <https://docs.mousepawmedia.com/pawlib/general/setup.html>`_.

Using Goldilocks: `Read the official docs <https://docs.mousepawmedia.com/pawlib/goldilocks/goldilocks.html>`_.


Development Tools
^^^^^^^^^^^^^^^^^^

IDE (Integrated Development Environment): Any multilingual IDE that floats your boat is recommended.

Compiler: GCC 6.4.0 and above, LLVM Clang 5.0, and MSVC.


Arcanist and Git
-----------------

`Arcanist <https://secure.phabricator.com/book/phabricator/article/arcanist/>`_

`Git <https://git-scm.com/docs>`_

Check out one of our repositories via Diffusion on Phabricator.
(You'll want to set up either a VCS Password or SSH Public
Key on your Phabricator Settings.)

Working on the Qub³d engine with Git/Arcanist:

On UNIX-like platforms, type from the command line after installing git:

..  code-block:: bash

    $ git clone https://github.com/qub3d/qub3dengine
    $ cd qub3dengine/

On your local copy of the repository, create a new branch via 
git checkout -b thenewbranchname

Make your changes, and then send them up:

..  code-block:: bash

    $ git add .
    $ git commit -m "<Insert Commit Summary>"
    $ arc diff

Your code will appear as a new Revision on Differential.
It will need to be reviewed and approved by a Trusted member.
If they request changes, do the following after making changes:

..  code-block:: bash

    $ git add .
    $ git commit -m "<Insert Problem Address>"
    $ arc diff

Then, the current diff will get updated to address the change
requests.

Git commit messages must be:

- Descriptive. (No "Update init.lua" or "Fix a problem.") You must tell
  the maintainers *why* you're making this commit in the first place.

- Concise. The hard limit of characters to be on the subject line is 50.

- Capitalized. All subjects must be capitalized. i.e. "Fix all Bugs with Goldilocks implemented"

- Free of spelling errors.

- In present tense. No "-ed" suffixes.

- Professional. No slang words, no incorporating personal opinions, and
  no grammatical errors. Professional acronyms such as "AFAIK" are allowed.

- Free of useless punctuation. No periods at the end of the subject line,
  for space is precious if you're trying to keep below 50 characters.

- Easy to understand. Type the commit messages as if you were talking to
  average person who knows nothing about your intentions.

Git commit bodies are also useful if you're submitting a fundamental launch.
The commit bodies' rules are the same as the commit messages but with two
more mandatory rules:

- Limit the amount of characters to 72.

- Tell the maintainer how your patch works in an efficiently descriptive manner.


Contributor Requirements
==============================

The following are the requirements to meet before contributing
to the project.


Code
-----

To contribute to the engine/launcher, you must have fair
knowledge of at least *one* of the following languages: 

C++, Lua, and YAML.

As they are the languages used in the engine/launcher.


Documentation
--------------

If you're just contributing to documentation, you should have the
following characteristics:

- Professional Working Proficiency (ILR Level 3) or better with English

- Knowledge of RST and its syntax

- Knowledge of Markdown (Only applicable if you're writing Markdown in the
  documentation)

NOTE: Having fair knowledge of English is mandatory if
working on documentation.


Rules
==============================

Below are the rules you must abide by when contributing
to the project.


Rules For Submitting Code
--------------------------

There are preliminary checks you must do on your branch before launching.
The diff must have the following characteristics:

(1) Accomplish the feature(s) it was designed to accomplish. [In some cases, the feature
itself may be dropped, and only bugfixes and/or optimizations landed instead.]

(2) Have merged all changes from `master` into itself, and all conflicts resolved. ($ git pull origin master)

(3) Have binaries and unnecessary cruft untracked and removed. (Keep an eye on .gitignore!)

(4) Compile and run properly.

(5) Be free of compiler errors and warnings (must compile with `-Wall -Wextra -Werror`).

(6) Be Valgrind pure (no memory leaks detected).

(7) Comply with Coding Standards/Style.

(8) Be free of linter errors. ($ arc lint --lintall)

(9) Be fully CSI commented.

(10) Have an up-to-date build script (generally CMake) if relevant.

(11) Contain relevant LIT tests, if the project is Goldilocks capable.

(12) Have a Test Plan, generally containing a list of Goldilocks tests the reviewer should run.

(13) Be reviewed, built, tested, and approved by at least one trusted reviewer
(Staff or Trusted Contributor).

(14) Have up-to-date Sphinx documentation, which compiles with no warnings.

(15) Have all reviewer comments processed and marked "Done".

(16) For bug fixes, please show a way of demonstrating that the
diff actually fixes something.

(17) If the contributor doesn't run the Goldilocks
test suite on the diff, then the maintainer will.

(18) If the diff fixes a bug reported in Ponder, a brief reference
to that bug must be included in the Summary.

(19) Have tests run by Jenkins CI pass properly.

(20) Have the reviewers: NewbProgrammer101 and TMcSquared.


If you are unfamiliar with CSI, `see the official documentation <https://standards.mousepawmedia.com/csi.html>`_.

You must also abide by the C++ and Lua coding standards/style provided by the Qub³d
Engine Group. For more information on our Coding Standards/Style, see the C++
Coding Standards Howto and the Lua Coding Standards Howto.

Before pushing any significant diff, please double check to see
if there is an issue with a :guilabel:`Help Wanted` tag that describes your
intention, has been approved, and was not assigned to anyone else. However,
if there is no such issue, `create a new one in Ponder <https://phab.qub3d.org/ponder>`_.
If there is an issue that wasn't assigned to anyone, simply leave a
comment behind stating that you wish to work on it, and a Trusted Member
will assign it to you, or you can scroll to the bottom of the issue web
page and click on :guilabel:`Actions...` and click on :guilabel:`Assign/Claim` to show others
that you are officially working on the issue. If you're submitting a
bug fix, documentation change, and/or other miniscule changes, there
is no need to create an issue, just launch the diff.

If Jenkins fails to pass the test properly, please find out why.
The Qub³d Engine Group will not let failed tests pass through the gates to
landing for any reason.


Rules For Submitting Documentation
-----------------------------------

See the Documentation Howto.


Miscellaneous
==============================

If you don't feel like hacking and/or documenting the Qub³d
engine/launcher, there's still plenty of other ways for you to help!
You can answer questions on the Discord Server and/or
`Ponder here <https://phab.qub3d.org/ponder>`_, find bugs, promote
Qub³d, contribute to the Qub³d official website, submit ideas in the
`Ideas Board <https://phab.qub3d.org/w/ideas>`_, help review a
diff, provide penetration test results for the qub3d.org server,
or give end-user feedback.


Post-Launch
==============================

You have launched your first diff, congratulations!


Now What?
----------

You wait for the diff to get reviewed. Once it is reviewed, you wait
for approval from the maintainers.


Troubleshooting
----------------


(Problem 1)
^^^^^^^^^^^^

You have launched a diff but it's being prevented by an HTTP
error 403. Fear not! `There's a solution here <https://phab.qub3d.org/Q1>`_.


Conclusion
==============================

While this may seem like a lot to abide by, it is beneficial for both
you and the Qub³d project. It also gets easier the more you contribute.

