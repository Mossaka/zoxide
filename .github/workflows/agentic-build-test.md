---
name: Agentic Build and Test
on:
  workflow_dispatch:
  push:
    branches: [main]
permissions:
  contents: read
  issues: read
  pull-requests: read
runtimes:
  rust: {}
network:
  allowed:
    - crates.io
    - static.crates.io
    - index.crates.io
    - github.com
    - api.github.com
    - static.rust-lang.org
engine: copilot
---

# Build and Test zoxide

Build and test the zoxide project (a smarter cd command) using Cargo.

## Tasks

1. Run `cargo build --release` to compile the project in release mode
2. Run `cargo test` to execute all unit tests
3. Run `cargo clippy` if available to check for common issues
4. Report any build errors or test failures with details

## Expected Outcome

All builds should succeed and all tests should pass. If there are any failures, provide detailed error messages and suggestions for fixes.
