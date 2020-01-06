# <img src="https://raw.githubusercontent.com/LiveSplit/LiveSplit/master/LiveSplit/Resources/Icon.png" alt="LiveSplit" height="42" width="45" align="top"/> LiveSplit One

[![Build Status](https://travis-ci.org/LiveSplit/LiveSplitOne.svg?branch=master)](https://travis-ci.org/LiveSplit/LiveSplitOne) [![Greenkeeper badge](https://badges.greenkeeper.io/LiveSplit/LiveSplitOne.svg)](https://greenkeeper.io/)

LiveSplit One is a version of LiveSplit that uses the multiplatform
[livesplit-core](https://github.com/LiveSplit/livesplit-core) Library and Web
Technologies like React to create a new LiveSplit experience that
works on a lot of different platforms.

The Web Version is available [here](https://one.livesplit.org/).

## Build Instructions

In order to build LiveSplit One you need to install
[npm](https://www.npmjs.com/get-npm) and the [Rust
Compiler](https://www.rust-lang.org/). Make sure to recursively clone the
repository so that all git submodules are cloned as well:

```bash
git clone --recursive
```

Once you have cloned the repository and both the Rust compiler and npm are set
up, you need to install the WebAssembly target like so:

```bash
rustup target add wasm32-unknown-unknown
```

You also need wasm-bindgen. You can build it like so:

```bash
cargo install wasm-bindgen-cli
```

You need to set up some npm modules before compiling the project:

```bash
npm install
```

You are now ready to build livesplit-core, which powers LiveSplit One:

```bash
npm run build:core
```

Now you can build and host LiveSplit One:

```bash
npm run start
```

A browser tab with LiveSplit One should now open. Alternatively you can use `npm
run serve` to just host it without opening a browser tab.

## Browser Support

| Browser           | Compatibility | Known Issues                                                                                                                                                                                                            |
| ----------------- | ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Chrome            | ≥57           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Google%20Chrome.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3A"Google%20Chrome")         |
| Firefox           | ≥52           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Firefox.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3AFirefox)                           |
| Edge              | ≥16           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Microsoft%20Edge.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3A"Microsoft%20Edge")       |
| Safari            | ≥11           |                                                                                                                                                                                                                         |
| Opera             | ≥44           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Google%20Chrome.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3A"Google%20Chrome")         |
| iOS               | ≥11.2         | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/iOS.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3AiOS)                                   |
| Android WebView   | ≥62           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Android.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3AAndroid)                           |
| Chrome Android    | ≥66           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Android.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3AAndroid)                           |
| Firefox Android   | ≥60           | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Android.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3AAndroid)                           |
| Internet Explorer | Unsupported   | [![GitHub issues by-label](https://img.shields.io/github/issues/LiveSplit/LiveSplitOne/Internet%20Explorer.svg)](https://github.com/LiveSplit/LiveSplitOne/issues?q=is%3Aissue+is%3Aopen+label%3A"Internet%20Explorer") |
| Opera Mini        | Unsupported   |                                                                                                                                                                                                                         |
