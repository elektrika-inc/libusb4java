## Overview

The purpose of this fork is to gather all the required build dependencies of `libusb4java`
into one place, to make building the native `usb4java.dll` easy:

* JNI headers
* LibUSB header and DLLs

## Building DLLs

Open the appropriate Visual Studio solution (ex. the one in `VS2017\libusb4java`) and
build release DLLs, which will be placed in `dist\$(PlatformTarget)\Release` under the
solution folder.

### Distribution

Note that the resulting `usb4java.dll` depends on both `libusb-1.0.dll` (which can be
found in the appropriate subfolder of `libusb`) and the appropriate [Visual Studio runtime
library][VCRUNTIME] (ex. `vcruntime140.dll`), which can be found in the `Redist` folder of
your Visual Studio installation; and thus these will have to be included with your
program.

<!-- References -->

[VCRUNTIME]: https://docs.microsoft.com/en-us/cpp/windows/determining-which-dlls-to-redistribute?view=msvc-160