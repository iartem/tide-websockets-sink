# tide-websockets-sink

> This is a fork of [https://github.com/http-rs/tide-websockets/](tide-websockets) that includes Sink trait contributions from the community ([#3](https://github.com/http-rs/tide-websockets/pull/3), [#9](https://github.com/http-rs/tide-websockets/pull/9)). It will be kept in **sync** with the upstream implementation. The scope of this library may grow depending upon whether community contributions in the upstream library are accepted. This will be the *"kitchen sink"* of misfit pull requests.

## experimental websockets handler for [tide](https://github.com/http-rs/tide) based on [async-tungstenite](https://github.com/sdroege/async-tungstenite)

* [API Docs][docs] [![docs.rs docs][docs-badge]][docs]
* [![crates.io version][version-badge]][lib-rs]

[docs]: https://docs.rs/tide-websockets-sink
[lib-rs]: https://lib.rs/tide-websockets-sink
[docs-badge]: https://img.shields.io/badge/docs-latest-blue.svg?style=flat-square
[version-badge]: https://img.shields.io/crates/v/tide-websockets-sink.svg?style=flat-square

## Installation
```sh
$ cargo add tide-websockets-sink
```

## Using with tide

This can either be used as a middleware or as an endpoint. If used as a middleware, the endpoint will be executed if the request is not a websocket upgrade. If used as an endpoint but the request is not a websocket request, tide will reply with a `426 Upgrade Required` status code.

see [the example](https://github.com/cryptoquick/tide-websockets-sink/blob/main/examples/example.rs) for the most up-to-date example of usage

## Safety
This crate uses ``#![deny(unsafe_code)]`` to ensure everything is implemented in
100% Safe Rust.

## Alternatives
- [tide-websockets-sink](https://github.com/cryptoquick/tide-websockets-sink) - A fork of this project that implements the Sink trait.

## License

<sup>
Licensed under either of <a href="LICENSE-APACHE">Apache License, Version
2.0</a> or <a href="LICENSE-MIT">MIT license</a> at your option.
</sup>

<br/>

<sub>
Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this crate by you, as defined in the Apache-2.0 license, shall
be dual licensed as above, without any additional terms or conditions.
</sub>

