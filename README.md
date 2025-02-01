# cpp-library-template

A simple template repository for creating C++ libraries, using CMake as a build system, Google Test as a testing framework,
and vcpkg for distribution, packaging, and dependency management.

## Usage

Clone/fork this repository, or use this repository as a template in GitHub/GitLab.
The template contains a `src/` directory for source files, and a `test/` directory for tests.

### Building

The template has a boilerplate CMake configuration, so the project can be built like any other
CMake project.

```
cmake --preset=default
cmake --build --preset=default
```

### Running tests

After building, tests can be run via CMake with:

```
cd build/
ctest
```

## Packaging and distributing your library

### Via vcpkg

### Via CMake

### Via Conan
Not currently supported, but contributions are welcome.

## License

This project is licensed under the MIT license.
