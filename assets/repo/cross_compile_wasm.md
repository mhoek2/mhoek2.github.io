### Cross-Compile WebAssembly - x86 x64
	tags[C++,OpenGL,Emscripten]
![cross-compile](assets/illustrations/wasm-cross-compile.png)

[![repo](https://img.shields.io/badge/View%20Repository-grey.svg?logo=github)](https://github.com/mhoek2/wasm-cross)
 [![build](https://github.com/mhoek2/wasm-cross/actions/workflows/build.yml/badge.svg)](https://github.com/mhoek2/wasm-cross/actions/workflows/build.yml)
 [![windows-binaries](https://img.shields.io/badge/Windows%20Binaries-cyan.svg)](https://github.com/mhoek2/wasm-cross/releases)
 [![live-demo](https://img.shields.io/badge/Live%20Demo-orange.svg)](https://mhoek2.github.io/wasm-cross/)


This demo shows a core principles of WebAssembly compiling using [Emscripten](https://emscripten.org/).

Displaying a rotating 3D model of the Earth using GLFW with OpenGL or GLES3-WebGL2.

I included **[Github CI](https://github.com/mhoek2/wasm-cross/blob/main/.github/workflows/build.yml)** to cross-compile for **WebAssembly** and a native **[Windows x86 & x64](https://github.com/mhoek2/wasm-cross/releases)** application.

> Emscripten compiles C and C++ to [WebAssembly](https://webassembly.org/) using
[LLVM](https://en.wikipedia.org/wiki/LLVM) and
[Binaryen](https://github.com/WebAssembly/binaryen/). The output can run
on the Web, in Node.js, and in
[wasm runtimes](https://v8.dev/blog/emscripten-standalone-wasm#running-in-wasm-runtimes).
It provides Web support for popular portable APIs such as OpenGL and
SDL2.