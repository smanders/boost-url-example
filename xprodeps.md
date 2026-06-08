# boost-url-example dependencies

|project|license [^_l]|description [dependencies]|version|source|diff [^_d]|
|-------|-------------|--------------------------|-------|------|----------|
|<a id='boost-url-example' />[boost-url-example](https://www.meetup.com/utah-cpp-programmers/events/313994701/)| |Manipulating URLs with Boost URL [deps: _boost_] [pvt deps: _googletest_]| |[upstream](https://github.com/LegalizeAdulthood/boost-url-example 'github.com/LegalizeAdulthood/boost-url-example')| |
|<a id='boost' />[boost](http://www.boost.org/ 'Boost website')|[BSL-1.0](http://www.boost.org/users/license.html 'Boost Software License')|libraries that give C++ a boost [deps: _bzip2, zlib_]|[xpv1.91.0.1](https://github.com/externpro/boost/releases/tag/xpv1.91.0.1 'release')|[repo](https://github.com/externpro/boost 'github.com/externpro/boost') [upstream](https://github.com/boostorg/boost 'github.com/boostorg/boost')|[diff](https://github.com/externpro/boost/compare/boost-1.91.0...xpv1.91.0.1 'github.com/externpro/boost/compare/boost-1.91.0...xpv1.91.0.1') [native]|
|<a id='googletest' />[googletest](https://google.github.io/googletest/)|[BSD-3-Clause](https://github.com/google/googletest/blob/master/LICENSE 'BSD 3-Clause New or Revised License')|GoogleTest - Google Testing and Mocking Framework [deps: _Threads_]|[xpv1.16.0.7](https://github.com/externpro/googletest/releases/tag/xpv1.16.0.7 'release')|[repo](https://github.com/externpro/googletest 'github.com/externpro/googletest') [upstream](https://github.com/google/googletest 'github.com/google/googletest')|[diff](https://github.com/externpro/googletest/compare/v1.16.0...xpv1.16.0.7 'github.com/externpro/googletest/compare/v1.16.0...xpv1.16.0.7') [patch]|
|<a id='bzip2' />[bzip2](https://sourceware.org/bzip2/)|[bzip2-1.0.6](https://spdx.org/licenses/bzip2-1.0.6.html 'BSD-like, modified zlib license')|lossless block-sorting data compression library|[xpv1.0.8.5](https://github.com/externpro/bzip2/releases/tag/xpv1.0.8.5 'release')|[repo](https://github.com/externpro/bzip2 'github.com/externpro/bzip2') [upstream](https://github.com/opencor/bzip2 'github.com/opencor/bzip2')|[diff](https://github.com/externpro/bzip2/compare/bzip2-1.0.8...xpv1.0.8.5 'github.com/externpro/bzip2/compare/bzip2-1.0.8...xpv1.0.8.5') [intro]|
|<a id='zlib' />[zlib](https://zlib.net/ 'zlib website')|[Zlib](https://zlib.net/zlib_license.html 'zlib/libpng license, see https://en.wikipedia.org/wiki/Zlib_License')|a general-purpose lossless data-compression library|[xpv1.3.2.1](https://github.com/externpro/zlib/releases/tag/xpv1.3.2.1 'release')|[repo](https://github.com/externpro/zlib 'github.com/externpro/zlib') [upstream](https://github.com/madler/zlib 'github.com/madler/zlib')|[diff](https://github.com/externpro/zlib/compare/v1.3.2...xpv1.3.2.1 'github.com/externpro/zlib/compare/v1.3.2...xpv1.3.2.1') [patch]|
|<a id='Threads' />[Threads](https://cmake.org/cmake/help/latest/module/FindThreads.html)|[LGPL-2.1-or-later](https://spdx.org/licenses/LGPL-2.1-or-later.html 'GNU Lesser General Public License v2.1 or later')|Finds and determines the thread library of the system for multithreading support|[xpv1.0.4](https://github.com/externpro/Threads/releases/tag/xpv1.0.4 'release')|[repo](https://github.com/externpro/Threads 'github.com/externpro/Threads')|[diff](https://github.com/externpro/Threads/compare/v0...xpv1.0.4 'github.com/externpro/Threads/compare/v0...xpv1.0.4') [bin]|

![deps](xprodeps.svg 'dependencies')

Dependency version check: all 5 parent-manifest versions match pinned versions.

|diff  |description|
|------|-----------|
|patch |diff modifies/patches existing cmake|
|intro |diff introduces cmake|
|auto  |diff adds cmake to replace autotools/configure/make|
|native|diff adds cmake but uses existing build system|
|bin   |diff adds cmake to repackage binaries built elsewhere|
|fetch |diff adds cmake and utilizes FetchContent|

[^_l]: see [SPDX License List](https://spdx.org/licenses/ '') for a list of commonly found licenses
[^_d]: see table above with description of diff
