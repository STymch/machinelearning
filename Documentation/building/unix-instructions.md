Building ML.NET on Linux and macOS
==========================================
## Building

1. Install the prerequisites ([Linux](#user-content-linux), [macOS](#user-content-macos))
2. Clone the machine learning repo `git clone https://github.com/dotnet/machinelearning.git`
3. Navigate to the `machinelearning` directory
4. Run the build script `./build.sh`

Calling the script `build.sh` builds both the native and managed code.

For more information about the different options when building, run `build.sh -?` and look at examples in the [developer-guide](../project-docs/developer-guide.md).

## Minimum Hardware Requirements
- 2GB RAM

## Prerequisites (native build)

### Linux

First, the package lists might need to be updated

`sudo apt-get update`

On Linux, the following components are needed

* CMake on the PATH
* Clang 3.5+ (same requirements as coreclr/corefx)
* All the requirements necessary to run .NET Core 2.0 applications
* libunwind
* curl

### macOS

macOS 10.12 or higher is needed to build dotnet/machinelearning.

On macOS a few components are needed which are not provided by a default developer setup:
* CMake

One way of obtaining CMake is via [Homebrew](http://brew.sh):
```sh
$ brew install cmake
```