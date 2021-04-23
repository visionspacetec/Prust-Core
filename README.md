
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

# Supported Services of PUS-C
Currently Prust-Core supports the following services from [PUS-C](https://ecss.nl/standard/ecss-e-st-70-41c-space-engineering-telemetry-and-telecommand-packet-utilization-15-april-2016/):
- ST[01] request verification
    |Code|Description|
    |-|-|
    TM[1,1] | successful acceptance verification report
    TM[1,2] | failed acceptance verification report
    TM[1,3] | successful start of execution verification report
    TM[1,4] | failed start of execution verification report
    TM[1,5] | successful progress of execution verification report
    TM[1,6] | failed progress of execution verification report
    TM[1,7] | successful completion of execution verification report
    TM[1,8] | failed completion of execution verification report
    TM[1,10] | failed routing verification report

- ST[03] housekeeping
    |Code|Description|
    |-|-|
    TC[3,1] | create a housekeeping parameter report structure
    TC[3,5] | enable the periodic generation of housekeeping parameter reports
    TC[3,6] | disable the periodic generation of housekeeping parameter reports
    TM[3,25] | housekeeping parameter report
    TC[3,27] | generate a one shot report for housekeeping parameter report structures


- ST[08] function management
    |Code|Description|
    |-|-|
    TC[8,1] | perform a function

# Testing
To do unit testing in std enter:
```
cargo test
```


# Example
An example usage can be found in [Prust-FreeRTOS](https://github.com/visionspacetec/Prust-FreeRTOS) for the [VST104](https://github.com/visionspacetec/VST104-Sierra).  
The document of the process can also be bound on the wiki: [How To Build On VST104](https://github.com/visionspacetec/Prust/wiki/How-To-Build-On-VST104)

