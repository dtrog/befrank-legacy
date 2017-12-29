BeFrank integration/staging tree
================================

http://www.befrank.site

Copyright (c) 2009-2013 Bitcoin  Developers
Copyright (c) 2011-2013 Litecoin Developers
Copyright (c) 2018 		BeFrank  Developers

What is BeFrank?
----------------

BeFrank is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2016 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the BeFrank client sofware, see http://www.befrank.info.

License
-------

BeFrank is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/befrank/befrank/tags) are created
regularly to indicate new official, stable release versions of BeFrank.

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

    qmake BITCOIN_QT_TEST=1 -o Makefile.test befrank-qt.pro
    make -f Makefile.test
    ./befrank-qt_test

