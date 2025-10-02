# SNAP Compiler (snapc) v1.0

Author: Andre Gray  
© 2008

`snapc` is a minimal synthesizer programming language compiler.  
It parses simple `.snap` files and generates a standalone C++ DSP program that outputs audio via PortAudio.

---

## Features

- Supports `SineOsc` with `freq` parameter.
- Connects a single output wire to `audio.out`.
- Generates `generated.cpp` ready for compilation.
- Written in C++03 for portability.
- Tested on Linux/macOS (requires PortAudio).

---

## Prerequisites

- C++ compiler (g++/clang++) supporting C++03
- CMake 2.6+
- [PortAudio](http://www.portaudio.com/)
  - Ubuntu/Debian: `sudo apt-get install portaudio19-dev`
  - macOS (Homebrew): `brew install portaudio`

---

## Build Instructions

```bash
mkdir build && cd build
cmake ..
make

## Notes

- Reference implementation; can be extended with additional oscillators, filters, envelopes.
- Uses a simple block-based audio process model.
- Classic C++03 style for maximum portability.

