Unify integration/staging tree
================================

https://www.unify.today

Copyright (c) 2009-2017 Bitcoin Developers
Copyright (c) 2017 Unify Developers

What is Unify?
----------------

Unify is a lite version of Bitcoin using proof-of-stake algorithm.
 - 1 minute block targets
 - 19,276,800 total coins
 - 1 coin per block + possible additional fee
 - 3000 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Unify client sofware, see https://www.unify.today.

License
-------

Unify is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Unify
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/unify-project/unify/tags) are created
regularly to indicate new official, stable release versions of Unify.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./unify-qt_test

