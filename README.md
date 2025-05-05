# Project template
This is a very simple project template for using alongside vcpkg.

## Using vcpkg
There are two ways of using vcpkg for C++ projects. Either through "Classic mode", or "Manifest mode".
Remember to configure the CMake toolchain to point correctly towards your installation of vcpkg.

### Manifest mode
For manifest mode, simply populate "vcpkg.json" with the desired libraries and versions for your project, and configure the correct triplet for your toolchain.
When you're finished configuring the manifest, simply call `vcpkg install` in the project folder (Make sure vcpkg is configured in your environment variables). The libraries will be installed into a local folder, which is already .gitignored

### Classic mode
For classic mode, remove vcpkg.json, and use vcpkg as normal.