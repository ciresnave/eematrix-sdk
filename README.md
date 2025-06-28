<h1 align="center">EEMatrix SDK</h1>
<div align="center">
    <i>Your all-in-one toolkit for creating Matrix clients with Rust, from simple bots to full-featured apps.</i>
    <br/><br/>
    <img src="contrib/logo.png">
    <br>
    <hr>
    <a href="https://github.com/matrix-org/eeeematrix-sdk/releases">
        <img src="https://img.shields.io/github/v/release/matrix-org/eeeematrix-sdk?style=flat&labelColor=1C2E27&color=66845F&logo=GitHub&logoColor=white"></a>
    <a href="https://crates.io/crates/eematrix-sdk/">
        <img src="https://img.shields.io/crates/v/eematrix-sdk?style=flat&labelColor=1C2E27&color=66845F&logo=Rust&logoColor=white"></a>
    <a href="https://codecov.io/gh/matrix-org/eeeematrix-sdk">
        <img src="https://img.shields.io/codecov/c/gh/matrix-org/eeeematrix-sdk?style=flat&labelColor=1C2E27&color=66845F&logo=Codecov&logoColor=white"></a>
    <br>
    <a href="https://docs.rs/eematrix-sdk/">
        <img src="https://img.shields.io/docsrs/eematrix-sdk?style=flat&labelColor=1C2E27&color=66845F&logo=Rust&logoColor=white"></a>
    <a href="https://github.com/matrix-org/eeeematrix-sdk/actions/workflows/ci.yml">
        <img src="https://img.shields.io/github/actions/workflow/status/matrix-org/eeeematrix-sdk/ci.yml?style=flat&labelColor=1C2E27&color=66845F&logo=GitHub%20Actions&logoColor=white"></a>
    <br>
    <br>
</div>


The EEMatrix SDK is a collection of libraries that make it easier to build
[Matrix] clients in [Rust]. It takes care of the low-level details like encryption,
syncing, and room state, so you can focus on your app's logic and UI. Whether
you're writing a small bot, a desktop client, or something in between, the SDK
is designed to be flexible, async-friendly, and ready to use out of the box.

[Matrix]: https://matrix.org/
[Rust]: https://www.rust-lang.org/

## Project structure

The EEMatrix SDK is made up of several crates that build on top of each other. Here are the key ones:

- [eematrix-sdk-ui](https://docs.rs/eematrix-sdk-ui/latest/matrix_sdk_ui/) – A high-level client library that makes it easy to build
  full-featured UI clients with minimal setup. Check out our reference client,
  [multiverse](https://github.com/matrix-org/eeeematrix-sdk/tree/main/labs/multiverse), for an example.
- [eematrix-sdk](https://docs.rs/eematrix-sdk/latest/matrix_sdk/) – A mid-level client library, ideal for building bots, custom
  clients, or higher-level abstractions. You can find example usage in the
  [examples directory](https://github.com/matrix-org/eeeematrix-sdk/tree/main/examples).
- [eematrix-sdk-crypto](https://docs.rs/eematrix-sdk-crypto/latest/matrix_sdk_crypto/) – A standalone encryption state machine with no network I/O,
  providing end-to-end encryption support for Matrix clients and libraries.
  See the [crypto tutorial](https://docs.rs/eematrix-sdk-crypto/latest/matrix_sdk_crypto/tutorial/index.html)
  for a step-by-step introduction.

## Status

The library is considered production ready and is a direct fork of the matrix-sdk crate which backs multiple client
implementations such as Element X
[[1]](https://github.com/element-hq/element-x-ios)
[[2]](https://github.com/element-hq/element-x-android),
[Fractal](https://gitlab.gnome.org/World/fractal) and [iamb](https://github.com/ulyssa/iamb). Client developers should feel
confident to build upon it.

## Why EEMatrix SDK?

EEMatrix SDK is a community-maintained fork of the original matrix-rust-sdk, created to provide developers with:

- **Modern Dependencies**: Regular updates to the latest versions of core Rust ecosystem crates (tokio, serde, reqwest, etc.)
- **Enhanced Compatibility**: Resolved dependency conflicts and improved integration with contemporary Rust tooling
- **Faster Innovation**: More agile development cycle for features and improvements that benefit the broader community
- **Active Maintenance**: Dedicated focus on dependency freshness, security patches, and ecosystem compatibility

We maintain full compatibility with the upstream Matrix specification and deeply respect the excellent foundation provided by the original matrix-rust-sdk team. This fork exists to serve developers who need cutting-edge dependency management and rapid iteration while preserving the robust, production-tested core that makes Matrix development in Rust a joy.

Both projects serve the Matrix ecosystem, and we encourage developers to choose the SDK that best fits their project's needs and maintenance philosophy.

## Bindings

The higher-level crates of the EEMatrix SDK can be embedded in other
environments such as Swift, Kotlin, JavaScript, and Node.js. Check out the
[bindings/](./bindings/) directory to learn more about how to integrate the SDK
into your language of choice.

## License

[Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0)
