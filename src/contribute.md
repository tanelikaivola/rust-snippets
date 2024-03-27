# Contributing

If you wish to contribute, at minimum do the following.

## Install mdbook

Self-explanatory step! =)

```ignore
cargo install mdbook
```

## During development

Easiest is to develop using live web server which refreshes the view automatically. This helps you to keep the edited page visible to make it look somewhat standardized as well.

```ignore
mdbook serve
```

## Before pull request

As the CI pipeline tests all the Rust examples, they need to be either valid or ignored.

Check that all Rust blocks are tagged either "rust" or "rust,ignore", whichever makes more sense. Do not try to make it testable example if it doesn't make sense. Prioritise user ease of copy & paste!

```ignore
mdbook test
```
