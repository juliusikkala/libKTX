Simplified libKTX
=================

Original: https://github.com/KhronosGroup/KTX-Software

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
have to use. It is licensed under the MIT license. It servers as a minimal
example of how to build the library, but you should probably just write build
scripts for your chosen build system.

As I've made a point of not touching the code at all, the rest of the code is
completely unmodified.

## Building

To build the library with the supplied Meson build file, run the below commands:

```sh
meson build
ninja -C build
```

The built library can then be found in `build/`.
