# mkcompletion

make `complete` script files from the configuration file.

## Overview

This project aims to convert the CLI parsing library source code from the configuration file.
For example, the JSON configuration file defines the arguments and options of some CLI tool,
`mkcompletion` converts it into the source codes of Java ([picocli](https://picocli.info)), 
Rust ([clap](https://docs.rs/clap/latest/clap/)), Go ([cobra](https://github.com/spf13/cobra)) and, etc.
These libraries have the feature for generating completion scripts.
Then, `mkcompletion` generates the completion scripts through these libraries.

From my experience, `clap` is currently the best solution, I think.
Because `clap` generates understandable `complete` scripts and supports `bash`, `zsh`, `fish`, `powershell`, and `elvish`.
Therefore, I will first define the JSON scheme for CLI option and arguments,
and then implement the converter for Rust (`clap`).


