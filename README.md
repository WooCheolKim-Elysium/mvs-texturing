# Building on Windows #

Building MVS-Texturing on Windows is possible, but unsupported. There are a few issues when compiling with Visual Studio which have been patched in the "cmake" branch of Andre Schulz' fork of MVS-Texturing (https://github.com/andre-schulz/mvs-texturing.git). A list of patched issues follows:

Replace GNU make build system with CMake
Downgraded OpenMP 3.0+ code back to 2.0 because Visual Studio only supports OpenMP 2.0

# Requirements #

1. 64-bit Windows

2. Visual Studio 2015 (64-bit) or newer

3. CMake 3.1 or newer

# Build instructions #

1. First, build MVE according to the MVE build instructions for Windows (https://github.com/simonfuhrmann/mve/wiki/Build-Instructions-for-Windows)

2. Pull from https://github.com/andre-schulz/mvs-texturing.git into a folder parallel to "mve". (i.e. if you cloned MVE into "/path/to/mve", then you should clone mvs-texturing into "/path/to/mvs-texturing")

3. Switch to the "cmake" branch (respectively "remotes/origin/cmake")

4. Run cmake (configure + generate) in "mvs-texturing" folder

5. Open "Texturing.sln"

6. Set your desired solution configuration (you'll most likely want "Release")

7. Build the solution

8. You can find the resulting binary in "apps/texrecon/<CMAKE_BUILD_TYPE>", where CMAKE_BUILD_TYPE is your chosen build type, i.e. one of { Release, Debug, RelWithDebInfo, MinSizeRel }.
