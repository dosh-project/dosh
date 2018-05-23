# DOSH

A CryptoNote based Cryptocurrency.

# About

The advent of the Dosh Cryptocurrency is a coherent outcome to the
prerequisite for a more decentralized untraceable digital cash. 

Dosh is a CryptoNote based Cryptocurrency that utilizes proof-of-work to keep the network secure.
CryptoNight is the hashing algorithm used in stance to keep the network fairly accessible and distributed.

By using Dosh, you prevent any entity from obtaining your transactional history as the default mechanics of Dosh is to
obfuscate your activity. Participants are effectively protected by Ring Signatures when sending and receiving funds.

# Purpose
Our endeavor is to establish Dosh as a privacy focused decentralized Cryptocurrency, with the use of
an Egalitarian proof-of-work system where all participants have equal voting rights within the network.

This coin is for the users of the network and should remain fairly distributed. All development stages will be voted and
funded by the community in the effort to improve the project.

# Conf
* 18.4 Million coins
* 120 seconds per block w/ 18 ES Factor
* POW - CryptoNight
* Type - CryptoNote
* Issue date - 1st March 2018

# Building Dosh

### Dependencies:
* GCC 4.7.3+
* CMake 2.8.6+
* Boost 1.55+
* (Windows only) - Microsoft Visual Studio 2017

### On Windows:

Download dependencies from:
* http://gcc.gnu.org/
* http://www.cmake.org/
* http://www.boost.org/
* http://www.microsoft.com/

Advanced options:
Parallel build: run `make -j<number of threads>' instead of `make'.
Debug build: run `make build-debug'.
Test suite: run `make test-release' to run tests in addition to building. Running `make test-debug' will do the same to the debug version.
Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++' before running `make'.

To build, change to a directory where this file is located, and run this commands:
* mkdir build
* cd build
* cmake -G "Visual Studio 15 Win64" ..

Then Build within Visual Studio.

### Ubuntu:

Install dependencies as follows:
* sudo apt-get update
* sudo apt-get install cmake libboost-all-dev build-essential

To build, change to the dosh directory and run `make'. The resulting executables can be found in dosh/build/release/src.

## Mac:

Install dependencies with brew:
* brew install boost
* brew install cmake

Install Xcode and Developer Tools

Finally, make sure you add the following line to your CMakeLists.txt to surpress some warnings:
* set (CMAKE_CXX_FLAGS "-w")

Then type 'make'

# Using Dosh

On Unix/Mac Terminal: 
* ./doshd --config dosh.conf

On Windows CMD: 
* doshd.exe --config dosh.conf


# Using Simplewallet
On Unix/Mac Terminal: 
* ./simplewallet --config dosh.conf

On Windows CMD: 
* simplewallet.exe --config dosh.conf


### Extras

To run a block explorer, simply clone from latest commit as the release binaries have not activated this feature.

Then make sure to add the following parameters to your dosh.conf file:
* rpc-bind-ip=0.0.0.0
* enable-blockchain-indexes=1
* enable-cors=*
* enable-blockexplorer=1
* rpc-bind-port=18333
