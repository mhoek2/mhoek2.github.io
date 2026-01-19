### Cross-Compile WebAssembly - x86 x64
	tags[C++,OpenGL,Emscripten]
![cross-compile](assets/illustrations/wasm-cross-compile.png)

[![repo](https://img.shields.io/badge/View%20Repository-grey.svg?logo=github)](https://github.com/mhoek2/wasm-cross)
 [![build](https://github.com/mhoek2/wasm-cross/actions/workflows/build.yml/badge.svg)](https://github.com/mhoek2/wasm-cross/actions/workflows/build.yml)
 [![windows-binaries](https://img.shields.io/badge/Windows%20Binaries-cyan.svg?labelColor=9ddbdb&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciICB2aWV3Qm94PSIwIDAgNTAgNTAiIHdpZHRoPSI1MHB4IiBoZWlnaHQ9IjUwcHgiPjxwYXRoIGQ9Ik0xOS44NTIgNy43NjFsLTE1IDIuMjVDNC4zNjIgMTAuMDg1IDQgMTAuNTA1IDQgMTF2MTJjMCAuNTUzLjQ0OCAxIDEgMWgxNWMuNTUyIDAgMS0uNDQ3IDEtMVY4Ljc1YzAtLjI5MS0uMTI3LS41NjctLjM0OC0uNzU4QzIwLjQzMiA3LjgwMyAyMC4xMzkgNy43MjEgMTkuODUyIDcuNzYxek00NS42NTIgNC4yNDJjLS4yMi0uMTg5LS41MTItLjI3MS0uODAxLS4yMzFsLTIxIDMuMTVDMjMuMzYyIDcuMjM1IDIzIDcuNjU1IDIzIDguMTVWMjNjMCAuNTUzLjQ0OCAxIDEgMWgyMWMuNTUyIDAgMS0uNDQ3IDEtMVY1QzQ2IDQuNzA5IDQ1Ljg3MyA0LjQzMyA0NS42NTIgNC4yNDJ6TTIwIDI2SDVjLS41NTIgMC0xIC40NDctMSAxdjEyYzAgLjQ5NS4zNjIuOTE1Ljg1Mi45ODlsMTUgMi4yNWMuMDUuMDA3LjA5OS4wMTEuMTQ4LjAxMS4yMzggMCAuNDctLjA4NS42NTItLjI0MkMyMC44NzMgNDEuODE3IDIxIDQxLjU0MSAyMSA0MS4yNVYyN0MyMSAyNi40NDcgMjAuNTUyIDI2IDIwIDI2ek00NSAyNkgyNGMtLjU1MiAwLTEgLjQ0Ny0xIDF2MTQuODVjMCAuNDk1LjM2Mi45MTUuODUyLjk4OWwyMSAzLjE1QzQ0LjkwMSA0NS45OTYgNDQuOTUxIDQ2IDQ1IDQ2Yy4yMzggMCAuNDctLjA4NS42NTItLjI0MkM0NS44NzMgNDUuNTY3IDQ2IDQ1LjI5MSA0NiA0NVYyN0M0NiAyNi40NDcgNDUuNTUyIDI2IDQ1IDI2eiIvPjwvc3ZnPg==)](https://github.com/mhoek2/wasm-cross/releases)
 [![live-demo](https://img.shields.io/badge/Live%20Demo-orange.svg?labelColor=db7645&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIiBmaWxsPSIjZmZmZmZmIj48IS0tIUZvbnQgQXdlc29tZSBGcmVlIHY2LjcuMiBieSBAZm9udGF3ZXNvbWUgLSBodHRwczovL2ZvbnRhd2Vzb21lLmNvbSBMaWNlbnNlIC0gaHR0cHM6Ly9mb250YXdlc29tZS5jb20vbGljZW5zZS9mcmVlIENvcHlyaWdodCAyMDI2IEZvbnRpY29ucywgSW5jLi0tPjxwYXRoIGQ9Ik00NjQgMjU2QTIwOCAyMDggMCAxIDAgNDggMjU2YTIwOCAyMDggMCAxIDAgNDE2IDB6TTAgMjU2YTI1NiAyNTYgMCAxIDEgNTEyIDBBMjU2IDI1NiAwIDEgMSAwIDI1NnpNMTg4LjMgMTQ3LjFjNy42LTQuMiAxNi44LTQuMSAyNC4zIC41bDE0NCA4OGM3LjEgNC40IDExLjUgMTIuMSAxMS41IDIwLjVzLTQuNCAxNi4xLTExLjUgMjAuNWwtMTQ0IDg4Yy03LjQgNC41LTE2LjcgNC43LTI0LjMgLjVzLTEyLjMtMTIuMi0xMi4zLTIwLjlsMC0xNzZjMC04LjcgNC43LTE2LjcgMTIuMy0yMC45eiIvPjwvc3ZnPg==)](https://mhoek2.github.io/wasm-cross/)


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