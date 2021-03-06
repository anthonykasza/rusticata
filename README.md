# Rusticata

[![Build Status](https://travis-ci.org/rusticata/rusticata.svg?branch=master)](https://travis-ci.org/rusticata/rusticata)

## Overview

Rusticata is a test crate for network protocol parsers written in Rust.

It was written to show to feasibility of the implementation of safe and efficient parsers
in suricata. The real parsing code is now part of suricata (starting from
version 4.0), and must be configured using the `--enable-rust` flag.

This project is now a playground for testing parsers, features and code.


This project is based on:
- [nom](https://github.com/Geal/nom) a Rust parser combinator framework
- Many parsers from the [rusticata project](https://github.com/rusticata)

## Build

Run `cargo build` for a build in debug mode, `cargo build --release` for release mode.

Use `cargo install` to install the library, or set the `LD_LIBRARY_PATH` environment variable.

## Testing

You need the [pcap-parse](https://github.com/rusticata/pcap-parse) tool.

```
git clone https://github.com/rusticata/pcap-parse.git
cd pcap-parse
```

Use `cargo build` to build the tool.

## Debug
`pcap-parse` uses the `RUST_LOG` environment variable to configure its output verbosity.
```
RUST_LOG=rusticata=Debug cargo run -- -p tls -f file.pcapng
```


## License

This library is licensed under the GNU Lesser General Public License version 2.1, or (at your option) any later version.
