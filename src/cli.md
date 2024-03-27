# Adding Command-Line Interface

Adds cli functionality.

## Cargo.toml

Default features for clap, sans color.

```sh,ignore
cargo add clap --no-default-features -F derive,cargo,error-context,help,std,suggestions,usage
```

## main.rs

```rust,ignore
mod cli;
use cli::{Cli, Parser};

fn main() {
    let args = Cli::parse();
...
}
```

## cli.rs

```rust,ignore
pub use clap::Parser;
use std::path::PathBuf;

/// Amazing command-line interface
#[derive(Parser, Debug)]
#[command(version, about, long_about = None)]
pub struct Cli {
	/// Process file
    pub path: PathBuf,
}
```

# More information

- [Clap Derive Tutorial](https://docs.rs/clap/latest/clap/_derive/_tutorial/chapter_0/index.html)
- [Clap Derive Reference](https://docs.rs/clap/latest/clap/_derive/index.html)