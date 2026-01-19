---
name: rust-coding-standards
description: Rust coding standards and best practices. Applies when writing, reviewing, or modifying Rust code.
---

# Rust Coding Standards

## Code Organization

- `use` statements must be at the beginning of the module, never within a function.

## Error Handling

- Propagate errors instead of returning default values - never fallback on failure.
- On unexpected failures (deserialization errors, function call errors, failed queries), propagate the error, never use defaults.
- Configuration values must not have hardcoded defaults (except for `Option`) - missing values are errors.

## String Conversions

- When converting `&str` to `String`, always use `.to_owned()` instead of `.to_string()`.
  Example: `"some_text".to_owned()` instead of `"some_text".to_string()`.

## Dependencies

- When adding dependencies, use the latest crate version unless instructed otherwise.

## Clippy

- When fixing clippy: run `cargo clippy --all-features --all-targets -- -Dwarnings` and fix all warnings.