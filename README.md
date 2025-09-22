# boinc-native-app

## Introduction

This repository contains a sample native BOINC application designed to run on various platforms. The application is built using CMake and supports multiple architectures and OSs:
- Android (ARM, ARM with NEON, ARM64, x86, x64)
- Linux (ARM, ARM64, x86, x64)
- macOS (ARM64, x64)
- Windows (x86, x64)

## Prerequisites

Before building the application, ensure you have the following tools installed:
- CMake (version 3.10 or higher)
- A C/C++ compiler compatible with your target platform (e.g., GCC, Clang, MSVC)

## Building the boinc-native-app application locally (for development and testing)

To build the boinc-native-app application, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/BOINC/boinc-native-app.git
   cd boinc-native-app
   ```
2. Bootstrap the project:

    For Unix-like systems (Linux, macOS):
   ```bash
   ./bootstrap.sh
   ```

    For Windows:
   ```bash
   bootstrap.bat
   ```

3. Create a build directory and navigate into it:
   ```bash
   mkdir build
   cd build
   ```

4. Configure the project using CMake:
   ```bash
   cmake ..
   ```

5. Build the application:
   ```bash
   cmake --build .
   ```

6. The compiled binaries will be located in the `build` directory.

## Building the boinc-native-app application using GitHub Actions (for release)

This repository includes a GitHub Actions workflow that automates the build process for multiple platforms. The workflow is defined in the `.github/workflows/build.yml` file.

To trigger the build process using GitHub Actions, simply push your changes to the repository or create a pull request. The workflow will automatically run and build the application for the specified platforms.

The build artifacts will be available in the "Actions" tab of the repository once the workflow completes.

It is recommended to fork the repository and enable GitHub Actions in your fork to customize the build process or add additional platforms.

## Modifying the boinc-native-app application

You can modify the source code of the boinc-native-app application.

All the application dependencies are managed using [vcpkg](https://vcpkg.io). To add new dependencies, update the `vcpkg.json` and `CMakeLists.txt` files accordingly.

After making changes, follow the build steps outlined above to compile the updated application.
