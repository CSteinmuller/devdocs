Contributors' Guide
###########################

25 Febuary 2018, 05:27 GMT

This file is dedicated to people who want to
contribute to the project but don't know what
Qub3d Engine Group's guidelines are.

You want to contribute to the project? Awesome!
Here, you will find out how to get started.

Create an account on our `Phabricator <`https://phab.qub3d.org>`_
using your GitHub account. If you don't have a GitHub
account, go ahead and create one. It's free, only takes
a couple minutes, and gives you access to the majority
of the open source development world!

Preliminary Keywords:

- Landing: Synonymous with merging.

- Launch: Synnonymous with Pull Request.


Getting Started
==============================

This section displays the guidelines for making a development
environment for the Qub3d project.


Development Environment
------------------------

For more expansion on this subsection, see section,
Development Workflow.

- Install `Cinder <`https://libcinder.org>`_ and `Goldilocks <https://goldilocks.org>`_. GOLDILOCKS.COM IS A DUMMY WEBSITE. DON'T RISK VISITING.

Cinder is the library that the Qub3d Engine requires
in order to work.

Goldilocks is the testing suite required by the
Qub3d Engine Group that is developed by MousepawMedia.

Installation of Cinder: download the archive and extract it.
Then, `cd` to the directory and run `cmake . -DCINDER_BOOST_USE_SYSTEM=1`
Once that's done, run `make -j<number of enabled threads>` to build.

Installation of Goldilocks: To be filled in later.


Arcanist and Git
-----------------

`Arcanist <`https://secure.phabricator.com/book/phabricator/article/arcanist/>`_.

`Git <`https://git-scm.com/docs>`_.

Check out one of our repositories via Diffusion on Phabricator.
(You'll want to set up either a VCS Password or SSH Public
Key on your Phabricator Settings.)

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
  the maintainers *why* you're making this commit in the message.

- Concise. The hard limit of characters to be on the subject line is 50.

- Capitalized. All subjects must be capitalized. i.e. "Fix all Bugs with Goldilocks implemented."

- Free of spelling errors.

- In present tense. No "-ed" suffixes.

- Professional. No slang words, no incorporating personal opinions, and
  no grammatical errors. Professional acronyms such as "AFAIK" are allowed.

- Free of useless punctuation. No periods at the end of the subject line,
  for space is precious if you're trying to keep below 50 characters.

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

C++, Lua, and JSON.

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
you want to make clear documentation.


Development Workflow
==============================

First, you are introduced to the developer-base:

- TMcSquared (Thomas Monroe/Tre): Lead Developer.
- NewbProgrammer101 (Jalus Bilieyich/Jay): Lead DevOp.
- CodeMouse92 (Jason C. McDonald): Lead Supervisor.

Each developer's workflow differs from another. If you want an
improved workflow, see below for examples.


Tre's Workflow
---------------


Jay's Workflow
---------------

He uses the `Pomodoro Method <`https://en.wikipedia.org/wiki/Pomodoro_Method>`_
as his default way of working on the Qub3d project.

He uses GNU Emacs as his IDE. If you want to see how he organizes
his system, take a look at his `UNIX dotfiles <`https://github.com/NewbProgrammer101/dotfiles>`_.

His overall workflow is very conservative.


Jason's Workflow
-----------------


Rules
==============================

Below are the rules you must abide by when contributing
to the project.


Rules For Submitting Code
--------------------------

Every Launch must have the reviewers: NewbProgrammer101 and TMcSquared.

There are preliminary checks you must do on your branch before launching.
They are:

(1) Accomplish the feature(s) it was designed to accomplish. [In some cases, the feature
itself may be dropped, and only bugfixes and/or optimizations landed instead.]

(2) Have merged all changes from `master` into itself, and all conflicts resolved. ($ git pull origin master)

(3) Have binaries and unnecessary cruft untracked and removed. (Keep an eye on .gitignore!)

(4) Compile and run properly.

(5) Be free of compiler errors and warnings (must compile with `-Wall -Wextra -Werror`).

(6) Be Valgrind pure (no memory leaks detected).

(7) Comply with Coding Standards.

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
testsuite on the patch, then the maintainer will.

(18) If the diff fixes a bug reported in Ponder, a brief reference
to that bug must be included in the Summary.

(19) Our CI, Jenkins, must pass the tests properly.


If you are unfamiliar with CSI, see the Commenting Showing Intent Howto.

You must also abide by the C++ and Lua code standards provided by the Qub3d Engine Group.
For more information on our Coding Standards, see the C++ Coding Standards Howto and
the Lua Coding Standards Howto.

Before pushing any significant diff, please double check to see
if there is an issue that describes your intention, the issue
has been approved, and was not assigned to anyone else. However,
if there is no such issue, create a new one in `Ponder <`https://phab.qub3d.org/ponder>`_.
If there is an issue that wasn't assigned to anyone, simply leave a
comment behind stating that you wish to work on it, and a Trusted Member
will assign it to you.

If you're submitting a bug fix, documentation change, and/or other
miniscule changes, there is no need to create an issue. Just launch the diff.

If Jenkins fails to pass the test properly, please find out why.
The Qub3d Engine Group will not let failed tests pass through the gates to
landing for any reason.


Rules For Submitting Documentation
-----------------------------------

See the Documentation Howto.


Miscellaneous
==============================

If you don't feel like hacking and/or documenting the Qub3d
engine/launcher, there's still plenty of other ways for you to help!
You can answer questions on the Discord Server and/or
`Ponder <`https://phab.qub3d.org/ponder>`_, find bugs, promote
Qub3d, contribute to the Qub3d official website, submit ideas in the
`Ideas Board <`https://phab.qub3d.org/w/ideas>`_, help review a
diff, or give end-user feedback.


Copyright Assignment
---------------------

Before submitting contributions, the Qub3d Engine Group will need
verification that you have signed the `ToD <`https://phab.qub3d.org/L2>`_.


Post-Launch
==============================

You have launched your first diff, congratulations!


Now What?
----------

You wait for the diff to get reviewed. Once it is reviewed, you wait
for approval from the maintainers.


Troubleshooting
----------------




Conclusion
==============================

While this may seem like a lot to abide by, it is beneficial for both
you and the Qub3d project. It also gets easier the more you contribute.
