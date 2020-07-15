License and Attribution Notices           {#license}
=======================

-----------------

This file has two names: LICENSE.md and NOTICE.md. The former to tell GitHub
users this is the license. The latter to tell creators of derived works that
they need to distribute this with or make it available in a display generated
by any Derivative Works, except for any parts that do not pertain to the
Derivative Work, in accordance with clause 4d of the Apache 2.0 license, i.e.
this is the "NOTICE" file.

Modifications by Julius Ikkala: removed ETC2-related files and other libraries.
Their licenses have also been removed from this file, since they are no longer
part of this distribution.

-----------------

## Default License

With the exception of the files listed explicitly below, the source is made
available under the Apache License, Version 2.0 (the "License"); you may not
use these files except in compliance with the License. You may obtain a copy of
the License at

&ensp;&ensp;&ensp;&ensp;http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

libKTX is the work of Mark Callow based on work by Georg Kolling and Jacob
Ström with contributions borrowed from Troy Hanson, Johannes van Waveren,
Lode Vandevenne and Rich Geldreich. The source contains code

    © 2010 ~ 2019 The Khronos Group Inc.
    © 2008 and © 2010 HI Corporation
    © 2005 Ericsson AB
    © 2003-2010, Troy D. Hanson
    © 2015-2020 Mark Callow
    © 2016 Oculus VR, LLC.
    © 2019 Binomial LLC. All Rights Reserved.
    © 2005-2019 Lode Vandevenne
    © 2019 Andreas Atteneder

The KTX load tests are the work of Mark Callow with a few small portions
borrowed from Sascha Willems' Vulkan examples and use Sam Lantinga's libSDL for 
portability. The source contains code

    © 2013 The Khronos Group Inc.
    © 2008 and © 2010 HI Corporation
    © 1997-2018 Sam Lantinga
    © 2016 Sascha Willems
    © 2015-2020 Mark Callow
    
`texturetests` and `unittests` are the work of Mark Callow and are based on gtest. The source contains code

    © 2010-2020 Mark Callow
    © 2006 Google Inc.
    
 `transcodetests` are the work of and were contributed by Andreas Atteneder.
 The source contains code
 
    © 2019 Andreas Atteneder

-----------------

**IMPORTANT:** Due to GitHub Markdown limitations license text has
been copied into this file from the files named below. In the event
of a discrepancy, the licenses in the files shall be deemed correct.

### uthash.h

uthash.h is made available under the following revised BSD license.

Copyright &copy; 2003-2010, Troy D. Hanson   http://uthash.sourceforge.net
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright
notice, this list of conditions and the following disclaimer.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS
IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER
OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
<<<<<<< HEAD
=======

### basisu/lodepng.[ch]

Copyright (c) 2005-2019 Lode Vandevenne

This software is provided 'as-is', without any express or implied
warranty. In no event will the authors be held liable for any damages
arising from the use of this software.

Permission is granted to anyone to use this software for any purpose,
including commercial applications, and to alter it and redistribute it
freely, subject to the following restrictions:

1. The origin of this software must not be misrepresented; you must not
    claim that you wrote the original software. If you use this software
    in a product, an acknowledgment in the product documentation would be
    appreciated but is not required.

2. Altered source versions must be plainly marked as such, and must not be
    misrepresented as being the original software.

3. This notice may not be removed or altered from any source
    distribution.

## Load Tests Exceptions

### icons/{ios/CommonIcons*,mac,win}/ktx_{app,document}.*

These KTX application and document icons are &copy; & &trade; The Khronos Group, Inc.
and may not be used without specific prior written permission from The Khronos Group,
except that the ktx_app icon may be distributed in a Derived Work as the icon for
the `glloadtests` and `vkloadtests` applications.

### other_include/SDL2/*

These files are part of the SDL2 source distributed by the [SDL project]
(http://libsdl.org) under the terms of the [zlib license]
(http://www.zlib.net/zlib_license.html).

### other_include/glm

OpenGL Mathematics is licensed under the [Happy Bunny (Modified MIT) License](https://github.com/g-truc/glm/blob/master/manual.md#section0)

### testimages/hi_mark{,_sq}.ktx

The HI logo textures are &copy; & &trade; HI Corporation and are
provided for use only in testing the KTX loader. Any other use requires
specific prior written permission from HI. Furthermore the name HI may
not be used to endorse or promote products derived from this software
without specific prior written permission.

### {VulkanMeshLoader,vulkantextoverlay}.hpp, vulkandebug.*

Copyright &copy; 2016 Sascha Willems - www.saschawillems.de

{VulkanMeshLoader,vulkantextoverlay}.hpp and vulkandebug.* are licensed
under the [MIT license](http://opensource.org/licenses/MIT)

## Other Test Exceptions

### gtest

Copyright 2006, Google Inc.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

* Redistributions of source code must retain the above copyright
notice, this list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above
copyright notice, this list of conditions and the following disclaimer
in the documentation and/or other materials provided with the
distribution.

* Neither the name of Google Inc. nor the names of its
contributors may be used to endorse or promote products derived from
this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.





>>>>>>> fc73f886063e979128d8790c75e5e5ede3e16dee
