# Solidify and generalize error handling code in the runtime

Error handling is a significant part of any project, historically we picked error-chain as an option for dealing with this, at the time it was the defacto standard in rust. This has changed by now and the project has grown to the point where error-chain can become cumbersome and maintain as an error handling framework. This project aims to solve this problem by taking the time to investigate alternatives and reset error handling to a fresh start.

### This comes with a few requirements:

1. Errors need to be helpful for users, this is the main priority.
2. Errors should be easy to add - in the past string errors have quickly crept in since adding new error cases was complicated and effort-intensive - simplifying this will lead to better maintainability
3. Support for hygienic errors especially for script failures (pointing to the location in the code) and hints
4. Support for structured logging
5. Accessibility - we should present errors in a way that is accessible to all users
6. Good cross crate support - the codebase includes a number of crates and we will need to be able to handle errors sensibly over crate boundaries
7. Performance is quite relevant, the error framework can not slow down execution on the hot path
8. A library or framework should be well maintained in the hope that it is long-lasting
9. Async support, while error handling is likely not affected by this it is worth keeping in mind since a lot of our code is async based
10. Ideally, error propagation and attribution to call paths would be helpful in many situations
11. Very optional, an ‘issue’ database, to link issues id’s to 

### A few related issues are:

* [investigate eyre as a replacement for error chain #389](https://github.com/tremor-rs/tremor-runtime/issues/389)
* [Streamline Logging and Error messages #508](https://github.com/tremor-rs/tremor-runtime/issues/508)
* [Use common error format and function for building errors #506](https://github.com/tremor-rs/tremor-runtime/issues/506)
* [`report.json` gets generated even when the -o flag isn't specified #1072](https://github.com/tremor-rs/tremor-runtime/issues/1072)

### Possible frameworks that have come to mind are (this is a non-exhaustive list):

ariadne
eyre (and color_eyre)
anyhow
