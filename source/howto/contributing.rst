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


Arcanist and Git
==============================

`Arcanist <`https://secure.phabricator.com/book/phabricator/article/arcanist/>`_.

`Git <`https://git-scm.com>`_.

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
    $ arc diff --update <Insert Current Differential>

Then, the current diff will get updated to address the change
requests.


Contributor Requirements
==============================

The following are the requirements to meet before contributing
to the project.


Code
-----

To contribute to the engine/launcher, you must have excellent
knowledge of the following:

- C++

- Lua

- JSON

As they are the languages used in the engine/launcher.


Documentation
--------------

If you're just contributing to documentation, you must have the
following characteristics:

- Excellent English

- Knowledge of RST

- Knowledge of Markdown (Only if you're writing Markdown in the
  documentation)

The above points are mandatory.


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

He follows the `Pomodoro Method <`https://en.wikipedia.org/wiki/Pomodoro_Method>`_
as his default way of working on the Qub3d project.

He uses GNU Emacs with org-mode as his IDE.

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
Every launch must also have the following subscriber: CodeMouse92.

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


If you are unfamiliar with CSI, see the Commenting Showing Intent Howto.

For more information on our Coding Standards, see the C++ Coding Standards Howto and
the Lua Coding Standards Howto.

You must also abide by the C++ and Lua code standards provided by the Qub3d Engine Group.


Rules For Submitting Documentation
-----------------------------------

See the Documentation Howto.


Conclusion
==============================

While this may seem like a lot to abide by, it is beneficial to both
you and the project. It also gets easier the more you contribute.
