
[![crates.io](https://img.shields.io/crates/v/prust_core.svg)](https://crates.io/crates/prust_core)
[![API](https://docs.rs/prust_core/badge.svg)](https://docs.rs/prust_core)
[![WIKI](https://img.shields.io/badge/wiki-prust-yellow.svg)](https://github.com/visionspacetec/Prust/wiki)
# Prust-Core
This crate is device independent and is designed to create and read [PUS-C](https://ecss.nl/standard/ecss-e-st-70-41c-space-engineering-telemetry-and-telecommand-packet-utilization-15-april-2016/) packets. This crate doesn't require rust-std.

# Requirements
Rust nightly is required. To change the channel you can type:
```
rustup default nightly   
```

# Feature
Currently Prust-Core supports the following services from [PUS-C](https://ecss.nl/standard/ecss-e-st-70-41c-space-engineering-telemetry-and-telecommand-packet-utilization-15-april-2016/):
- ST[01] request verification
- ST[03] housekeeping (partially)
- ST[08] function management

# Testing
To do unit testing in std enter:
```
cargo test
```


# Example
An example usage can be found in [Prust-FreeRTOS](https://github.com/visionspacetec/Prust-FreeRTOS) for the [VST104](https://github.com/visionspacetec/VST104-Sierra).  
The document of the process can also be bound on the wiki: [How To Build This On VST104](https://github.com/visionspacetec/Prust/wiki/How-To-Build-This-On-VST104)

