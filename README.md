# syn
> Generalized DNA for building real-time shared-state hApps on holochain

Syn: Etymology. From Ancient Greek συμ- (sum-), variant of συν- (sun-), from σύν (sún, “with, in company with, together with”).

## Design

Read the [design documents here](DESIGN.md).

## Prerequisites

- Build the Holochain tools
  - Clone the repo: `git clone https://github.com/holochain/holochain && cd ./holochain`
  - Ensure correct version of rust tool-chain via nix: `nix-shell`
  - Install conductor binary & dna-util binary:
``` bash
cargo install --path crates/holochain
cargo install --path crates/dna_util
```
  - Make sure the `path/to/holochain/.cargo/bin` is in your `PATH`

## Building

- Build the DNA (assumes you are still in the nix shell for correct rust/cargo versions from step above):
  - Clone this repo: `git clone https://github.com/holochain/syn && cd ./syn
  - Assemble the DNA:

  ```bash
  make build
  ```

  ### Testing

  ```bash
  make test
  ```

  #### Unit testing

  The `make test-unit` command runs all the unit tests for zomes in cargo.

  #### dna tryorama testing

  The `make test-dna` command packages/installs a fresh DNA and @holochain/tryorama tests it.

  ### Flushing 💩

  The `make clean` command gets rid of all compiled output.

  ## License
[![License: CAL 1.0](https://img.shields.io/badge/License-CAL%201.0-blue.svg)](https://github.com/holochain/cryptographic-autonomy-license)

  Copyright (C) 2017-2020, Holochain Foundation

This program is free software: you can redistribute it and/or modify it under the terms of the license
provided in the LICENSE file (CAL-1.0).  This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
