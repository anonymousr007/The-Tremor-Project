# The Tremor Project

## Pathway to do Error Handling in our project 

> Is anything missing or wrong please tell me :)

- [ ] Take a look an error handling of `rust` or `erlang` languages.
- [ ] Compare different crates such as [`eyre`](https://github.com/yaahc/eyre), [`color_eyre`](https://github.com/yaahc/color-eyre), [`anyhow`](https://github.com/dtolnay/anyhow) or [`thiserror`](https://github.com/dtolnay/thiserror) and find the most suitable crate for our tremor project.
- [ ] Make a list of error types [**very important**].
- [ ] [`linkerd2-proxy`](https://github.com/linkerd/linkerd2-proxy) has a similar project structure to ours and uses `thiserror` for error handling. So, Can we first study on this project `error handling system` ?
- [ ] Take a look of our `error-handling-system` and start implementing the best suitable crate for error handler.

## Crates for error-handling

* **anyhow**: Flexible concrete Error type built on std::error::Error.
* **color_eyre**: Custom hooks for colorful human oriented error reports via panics and the eyre crate.
* **eyre**: A trait object based error handling type for easy idiomatic error handling and reporting in Rust applications.
* **thiserror**: derive(Error) for struct and enum error types.

## Tremor Issues

* [investigate eyre as a replacement for error chain `#389`](https://github.com/tremor-rs/tremor-runtime/issues/389)
* [Use common error format and function for building errors `#506`](https://github.com/tremor-rs/tremor-runtime/issues/506)
* [Streamline Logging and Error messages `#508`](https://github.com/tremor-rs/tremor-runtime/issues/508)
* [Solidify and generalize error handling code in the runtime `#1175`](https://github.com/tremor-rs/tremor-runtime/issues/1175)

## Tremor Websites

* [Official Website](https://www.tremor.rs/)
* [Tremor Official Documentation](https://docs.tremor.rs/)
* [Tremor RFCS Website](https://rfcs.tremor.rs/)

## License

[Apache License 2.0](https://github.com/anonymousr007/Tremor-Notes/blob/main/LICENSE)
