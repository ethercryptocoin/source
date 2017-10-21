Compiling/running ethercryptocoind unit tests
------------------------------------

ethercryptocoind unit tests are in the `src/test/` directory; they
use the Boost::Test unit-testing framework.

To compile and run the tests:

	cd src
	make -f makefile.unix test_ethercryptocoin  # Replace makefile.unix if you're not on unix
	./test_ethercryptocoin   # Runs the unit tests

If all tests succeed the last line of output will be:
`*** No errors detected`

To add more tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections (the makefiles are
set up to add test/*.cpp to test_ethercryptocoin automatically).


Compiling/running EtherCryptoCoin-Qt unit tests
---------------------------------------

EtherCryptoCoin-Qt unit tests are in the src/qt/test/ directory; they
use the Qt unit-testing framework.

To compile and run the tests:

	qmake ethercryptocoin-qt.pro BITCOIN_QT_TEST=1
	make
	./ethercryptocoin-qt_test

To add more tests, add them to the `src/qt/test/` directory,
the `src/qt/test/test_main.cpp` file, and ethercryptocoin-qt.pro.
