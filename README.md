# cpp_to_rust

[![Linux + OS X](https://travis-ci.org/rust-qt/cpp_to_rust.svg?branch=master)](https://travis-ci.org/rust-qt/cpp_to_rust)
[![Windows](https://ci.appveyor.com/api/projects/status/m4yo29j2f5wfu3w0/branch/master?svg=true)](https://ci.appveyor.com/project/Riateche/cpp-to-rust)

`cpp_to_rust` allows to use C++ libraries from Rust. The main target of this project is Qt.

## Directions

*(Coming soon. Latest versions of Qt crates are not published yet.)*

If you just want to use Qt crates, add them as dependencies to your `Cargo.toml` and see the crates' documentation for more information.

[Online documentation](#) of published Qt crates 

Published crates required a certain Qt version (currently 5.8) and don't export platform-specific API.

If you want to use another Qt version, access platform-specific Qt APIs or tweak the generator configuration, refer to README of [qt_generator](https://github.com/rust-qt/cpp_to_rust/tree/master/qt_generator/qt_generator) for more information.

If you want to generate Rust crates for another C++ library or learn about implementation details, see README of [cpp_to_rust_generator](https://github.com/rust-qt/cpp_to_rust/tree/master/cpp_to_rust/cpp_to_rust_generator).

## Repository structure

The project consists of the following Rust crates:

- [cpp_to_rust/cpp_to_rust_generator](https://github.com/rust-qt/cpp_to_rust/tree/master/cpp_to_rust/cpp_to_rust_generator) implements the generator;
- [cpp_to_rust/cpp_to_rust_build_tools](https://github.com/rust-qt/cpp_to_rust/tree/master/cpp_to_rust/cpp_to_rust_build_tools) implements the build script for generated crates;
- [cpp_to_rust/cpp_to_rust_common](https://github.com/rust-qt/cpp_to_rust/tree/master/cpp_to_rust/cpp_to_rust_common) contains common code for the previous two crates;
- [cpp_to_rust/cpp_utils](https://github.com/rust-qt/cpp_to_rust/tree/master/cpp_to_rust/cpp_utils) provides essential utilities used by generated crates;
- [qt_generator/qt_generator](https://github.com/rust-qt/cpp_to_rust/tree/master/qt_generator/qt_generator) contains generator configuration for the Qt crates and a binary file for running the generator;
- [qt_generator/qt_build_tools](https://github.com/rust-qt/cpp_to_rust/tree/master/qt_generator/qt_build_tools) implements the advanced build script for Qt crates;
- [qt_generator/qt_generator_common](https://github.com/rust-qt/cpp_to_rust/tree/master/qt_generator/qt_generator_common) contains common code for the previous two crates.

See `README.md` in each crate for detailed description.

## Contributing

Contributions are always welcome! You can contribute in different ways:

- Suggest a C++ library to adapt;
- Submit a bug report, a feature request, or an improvement suggestion at the [issue tracker](https://github.com/rust-qt/cpp_to_rust/issues);
- Write a test for `cpp_to_rust_generator` crate;
- Write a test or an example for a Qt crate (porting examples from the official Qt documentation is a good option);
- Pick up an issue with [help wanted](https://github.com/rust-qt/cpp_to_rust/labels/help%20wanted) tag or any other issue you like.
