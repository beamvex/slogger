# slogger

A simple, colorful logging library for Rust applications with built-in ANSI terminal colors and formatted output.

## Features

- Colored log levels (DEBUG, INFO, WARN, ERROR)
- Timestamp in ISO 8601 format
- File and line number information
- Thread ID tracking
- Built-in ANSI color constants
- Easy-to-use macros for logging and color manipulation

## Installation

Add this to your `Cargo.toml`:

```toml
[dependencies]
slogger = "0.1.2"
```

## Usage

```rust
use slogger::{debug, info, warn, error};

fn main() {
    debug!("This is a debug message");    // Green
    info!("This is an info message");     // Blue
    warn!("This is a warning message");   // Yellow
    error!("This is an error message");   // Red
}
```

Each log message includes:
- Timestamp in ISO 8601 format
- Log level with color
- Source file and line number
- Thread ID
- Your message in the corresponding level color

## Color Utilities

The library also provides direct access to ANSI color codes and formatting:

```rust
use slogger::{green, blue, yellow, red};
use slogger::{green_start, blue_start, yellow_start, red_start};
use slogger::{bold_start, white_start, reset, colour_end};

println!("{}", green!("This text is green"));
```

## License

MIT License

## Links

- [Documentation](https://docs.rs/slogger)
- [Repository](https://github.com/beamvex/slogger)
- [Homepage](https://github.com/beamvex/slogger)
