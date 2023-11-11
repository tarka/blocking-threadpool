# blocking-threadpool

A thread pool for running a number of jobs on a fixed set of worker threads,
with optional back-pressure for job submission.

This project is a fork of
[rust-threadpool](https://github.com/rust-threadpool/rust-threadpool) with
back-pressure support added and minor maintenance improvements.

[![doc.rs](https://docs.rs/blocking-threadpool/badge.svg)](https://docs.rs/threadpool)

## Usage

Add this to your `Cargo.toml`:

```toml
[dependencies]
blocking-threadpool = "1.0"
```

## Minimal requirements

This crate requires Rust >= 1.13.0

## Memory performance

Rust [1.32.0](https://blog.rust-lang.org/2019/01/17/Rust-1.32.0.html) has switched from jemalloc to the operating systems allocator.
While this enables more plattforms for some workloads this means some performance loss.

To regain the performance consider enabling the [jemallocator crate](https://crates.io/crates/jemallocator).

## Similar libraries

* [rust-threadpool](https://github.com/rust-threadpool/rust-threadpool)
* [rayon (`rayon::ThreadPool`)](https://docs.rs/rayon/*/rayon/struct.ThreadPool.html)
* [rust-scoped-pool](http://github.com/reem/rust-scoped-pool)
* [scoped-threadpool-rs](https://github.com/Kimundi/scoped-threadpool-rs)
* [crossbeam](https://github.com/aturon/crossbeam)

## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in the work by you, as defined in the Apache-2.0
license, shall be dual licensed as above, without any additional terms or
conditions.
