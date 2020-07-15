Simplified libKTX
=================

Original: https://github.com/KhronosGroup/KTX-Software

<<<<<<< HEAD
This project is Khronos' libKTX, but in a form that is easier to integrate into
other projects. I have removed examples, tests, external libraries and their
headers (needed by those examples & tests) and all kinds of "cruft" that aren't
necessary when not working on KTX itself.

I have also removed Ericsson's ETC2-related code (`lib/etcdec.cxx` &
`lib/etcunpack.cxx` in the original repository) due to their dubious licensing.
Because of this, the library will have to be built with 
`-DSUPPORT_SOFTWARE_ETC_UNPACK=0`, or else you will have linking problems.
You can see the remaining license info at `LICENSE.md`.

The only actual code that is made by me here is `meson.build`, which you do not
have to use. It is licensed under the MIT license. It serves as a minimal
example of how to build the library, but you should probably just write build
scripts for your chosen build system.
=======
> **Note:** Visual Studio 2019 v16.5 & v16.6 get an internal compiler error when compiling parts of this software. v16.4 is okay. For Windows we suggest using Visual Studio 2017 until Microsoft fixes this bug.

> **Note:** This repo has just switched from a GYP-based to a CMake-based build system. The pre-generated build files have been removed but the .gyp files will remain available for a while and can be used to generate build files, using the GNUMakefile in the root of the project, in the event of a problem. You will have to install
[GYP](https://github.com/msc-/gyp/tree/remaster).

| GNU/Linux, iOS & OSX |  Windows | Documentation | 
|----------------------| :------: | :-----------: |
| [![Build Status](https://travis-ci.com/KhronosGroup/KTX-Software.svg?branch=master)](https://travis-ci.com/KhronosGroup/KTX-Software) | [![Build status](https://ci.appveyor.com/api/projects/status/rj9bg8g2jphg3rc0/branch/master?svg=true)](https://ci.appveyor.com/project/msc-/ktx/branch/master) | [![Build status](https://codedocs.xyz/KhronosGroup/KTX-Software.svg)](https://codedocs.xyz/KhronosGroup/KTX-Software/) |

This is the official home of the source code
for the Khronos KTX library and tools.

KTX (Khronos Texture) is a lightweight container for textures for OpenGL<sup>®</sup>, Vulkan<sup>®</sup> and other GPU APIs. KTX files contain all the parameters needed for texture loading. A single file can contain anything from a simple base-level 2D texture through to a cubemap array texture with mipmaps. Contained textures can be in a Basis Universal format, in any of the block-compressed formats supported by OpenGL family and Vulkan APIs and extensions or in an uncompressed single-plane format. Basis Universal currently encompasses two formats that can be quickly transcoded to any GPU-supported format: LZ/ETC1S, which combines block-compression and supercompression, and UASTC, a block-compressed format. Formats other than LZ/ETC1S can be supercompressed with Zstd.

The software consists of: (links are to source folders in the KhronosGroup repo)

- *libktx* - a small library of functions for writing and reading KTX
files, and instantiating OpenGL®, OpenGL ES™️ and Vulkan® textures
from them. [`lib`](https://github.com/KhronosGroup/KTX-Software/tree/master/lib)
- *libktx.{js,wasm}* - Web assembly version of libktx and
Javascript wrapper. [`interface/js_binding`](https://github.com/KhronosGroup/KTX-Software/tree/master/interface/js_binding)
- *msc\_basis\_transcoder.{js,wasm}* - Web assembly transcoder and
Javascript wrapper for Basis Universal formats. For use with KTX parsers written in Javascript. [`interface/js_binding`](https://github.com/KhronosGroup/KTX-Software/tree/master/interface/js_binding)
- *ktx2check* - a tool for validating KTX Version 2 format files. [`tools/ktx2check`](https://github.com/KhronosGroup/KTX-Software/tree/master/tools/ktx2check)
- *ktx2ktx2* - a tool for converting a KTX Version 1 file to a KTX
Version 2 file. [`tools/ktx2ktx2`](https://github.com/KhronosGroup/KTX-Software/tree/master/tools/ktx2ktx2)
- *ktxinfo* - a tool to display information about a KTX file in
human readable form. [`tools/ktxinfo`](https://github.com/KhronosGroup/KTX-Software/tree/master/tools/ktxinfo)
- *ktxsc* - a tool to supercompress a KTX Version 2 file that
contains uncompressed images.[`tools/ktxsc`](https://github.com/KhronosGroup/KTX-Software/tree/master/tools/ktxsc)
- *toktx* - a tool to create KTX files from PNG, Netpbm or JPEG format images. It supports mipmap generation, encoding to
Basis Universal formats and Zstd supercompression.[`tools/toktx`](https://github.com/KhronosGroup/KTX-Software/tree/master/tools/toktx)

Downloadable binary packages of the tools, library and development
headers are available at
[Releases](https://github.com/KhronosGroup/KTX-Software/releases).
There are also packages with the Javascript wrappers and .wasm binaries.

See the Doxygen generated [live documentation](https://github.khronos.org/KTX-Software/)
for API and tool usage information.
>>>>>>> fc73f886063e979128d8790c75e5e5ede3e16dee

As I've made a point of not touching the code at all, the rest of the code is
completely unmodified.

## Building

To build the library with the supplied Meson build file, run the below commands:

<<<<<<< HEAD
```sh
meson build
ninja -C build
=======
<!--
More information about KTX and links to tools that support it can be
found on the
[KTX page](http://www.khronos.org/opengles/sdk/tools/KTX/) of
the [OpenGL ES SDK](http://www.khronos.org/opengles/sdk) on
[khronos.org](http://www.khronos.org).
-->

If you need help with using the KTX library or KTX tools, please use the
[KTX forum](https://community.khronos.org/c/other-standards/ktx/).
To report problems use GitHub [issues](https://github.com/KhronosGroup/KTX/issues).

**IMPORTANT:** you **must** install the [Git LFS](https://github.com/github/git-lfs)
command line extension in order to fully checkout this repository after cloning. You
need at least version 1.1. If you did not have Git LFS installed at first checkout
then, after installing it, you **must** run

```bash
git lfs checkout
```

A few files have `$Date$` keywords. If you care about having the proper
dates shown or will be generating the documentation or preparing
distribution archives, you **must** follow the instructions below.

#### <a id="kwexpansion"></a>$Date$ keyword expansion

$Date$ keywords are expanded via a smudge & clean filter. To install
the filter, issue the following commands in the root of your clone.

On Unix (Linux, Mac OS X, etc.) platforms and Windows using Git for Windows'
Git Bash or Cygwin's bash terminal:

```bash
./install-gitconfig.sh
rm TODO.md include/ktx.h tools/toktx/toktx.cpp
git checkout TODO.md include/ktx.h tools/toktx/toktx.cpp
>>>>>>> fc73f886063e979128d8790c75e5e5ede3e16dee
```

The built library can then be found in `build/`.
