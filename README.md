What is ADVobfuscator?
======================

ADVobfuscator demonstates how to use C++11 language to generate, at compile time, obfuscated code without using any external tool and without modifying the compiler. The technics presented rely only on C++11, as standardized by ISO. It shows also how to introduce some form of randomness to generate polymorphic code and it gives some concrete examples like the encryption of strings literals and the obfuscation of calls using finite state machines.


News
====

ADVobfuscator code and whitepaper have been updated for BlackHat Europe 2014. It contains several improvements regarding obfuscation using finite state machines, combined with debugger detection (with an example of implementation for Mac OS X and iOS). To install Boost, use your favorite package manager. For example:

- Debian / Ubuntu: sudo apt-get install libboost-all-dev
- Mac OS X:  brew install boost


Prerequisites
=============

You have to install Boost library (www.boost.org) in order to use ADVdetector (it is used by FSM). Alternatively, you can comment out lines related to ObfuscatCall* (includes and code) in main.cpp.


Files
=====

- DetectDebugger.cpp				Debugger detection, implemented for Mac OS X and iOS. It is used by ObfuscatedCallWithPredicate (FSM)
- DetectDebugger.h					Debugger detection, declaration
- Indexes.h							Generate list of indexes at compile time (0, 1, 2, ... N)
- Log.h								Helper to log messages
- MetaFactorial.h					Compute factorial at compile time
- MetaFibonacci.h					Compute fibonacci sequence at compile time
- MetaFSM.h							Template to generate Finite State Machines at compile time
- MetaRandom.h						Generate a pseudo-random number at compile time
- MetaString1.h						Obfuscated string - version 1
- MetaString2.h						Obfuscated string - version 2 - Remove truncation
- MetaString3.h						Obfuscated string - version 3 - Random key
- MetaString4.h						Obfuscated string - version 4 - Random encryption algorithm
- ObfuscatedCall.h					Obfuscate function call
- ObfuscatedCallWithPredicate.h		Obfuscate function call, execute a FSM based on a predicate (such as DetectDebugger)
- main.cpp							Samples
- ADVobfuscator.xcodeproj			Project for Apple Xcode
- CompileWithGcc.sh					Simple script to compile for GCC


Copyright and license
=====================

Written by Sebastien Andrivet

Copyright (c) 2010-2014 - Sebastien Andrivet
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.