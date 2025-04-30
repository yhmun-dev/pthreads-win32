# PTHREADS-WIN32

Pthreads-win32 is free software, distributed under the GNU Lesser General Public License (LGPL). See the file 'COPYING.LIB' for terms and conditions. Also see the file 'COPYING' for information specific to pthreads-win32, copyrights and the LGPL.

To get more details, see [README](README) or go to [https://sourceware.org/pthreads-win32/](https://sourceware.org/pthreads-win32/)

![Build status](https://github.com/yhmun-dev/pthreads-win32/actions/workflows/build_action.yml/badge.svg)

### Build Requirements
  - [Meson 1.1.0 or later](https://mesonbuild.com/Getting-meson.html)
  - [Ninja](https://ninja-build.org)

### Build Instructions
  - __Configure__
    - Run `meson setup build/ [--buildtype debug|release] [--backend=<vs2022 or older>]`
    - Add `-Denable_test=true` if test is desired
  - __Compile__
    - Run `meson compile -C build/`
  - __Install__
    - Run `meson install -C build/`
  - __Test__
    - Run `meson test -C build/`
