[![discord](https://img.shields.io/discord/703636892901441577?logo=discord "Discord")](https://discord.gg/SHVaVfV)

# FastNoise Lite

[Web Preview App](https://auburn.github.io/FastNoiseLite)

FastNoise Lite is an extremely portable open source noise generation library with a large selection of noise algorithms. This library focuses on high performance while avoiding platform/language specific features, allowing for easy ports to as many possible languages.

This project is an evolution of the [original FastNoise](https://github.com/Auburn/FastNoiseLite/tree/FastNoise-Legacy) library and shares the same goal: An easy to use library that can quickly be integrated into a project and provides performant modern noise generation. See a breakdown of changes from the transition to FastNoise Lite [here](https://github.com/Auburn/FastNoiseLite/pull/49)

If you are looking for a more extensive noise generation library consider using [FastNoise2](https://github.com/Auburn/FastNoise2). It provides large performance gains thanks to SIMD and uses a node graph structure to allow complex noise configurations with lots of flexibility.

## Features

- 2D & 3D sampling
- OpenSimplex2 noise
- OpenSimplex2S noise
- Cellular (Voronoi) noise
- Perlin noise
- Value noise
- Value Cubic noise
- OpenSimplex2-based domain warp
- Basic Grid Gradient domain warp
- Multiple fractal options for all of the above
- Supports floats and/or doubles

### Supported Languages

- [C#](/CSharp/)
- [C++98](/Cpp/)
- [C99](/C/)
- [HLSL](/HLSL/)
- [GLSL](/GLSL/)
- [Go](/Go/)
- [Java](/Java/)
- [JavaScript](/JavaScript/)  
  [![npm](https://img.shields.io/npm/v/fastnoise-lite?logo=npm "npm")](https://www.npmjs.com/package/fastnoise-lite)
- [Rust](/Rust/)  
  [![crates.io](https://img.shields.io/crates/v/fastnoise-lite?logo=rust "crates.io")](https://crates.io/crates/fastnoise-lite)
- [Fortran](/Fortran/)
- [Zig](/Zig/)
- [PowerShell](/PowerShell/)
- [Odin](/Odin/)
- [Haxe](/Haxe/)
- [Pascal](/Pascal/)
- [GML](/GML/)

If you want to port FastNoise Lite to a new language create a pull request or discuss it on the discord linked above

### [Getting Started](https://github.com/Auburn/FastNoiseLite/wiki#getting-started)
### [Documentation](https://github.com/Auburn/FastNoiseLite/wiki/Documentation)

## FastNoise Lite Web Preview App

Link: [https://auburn.github.io/FastNoiseLite](https://auburn.github.io/FastNoiseLite)

A compact testing application is available for testing all features included in FastNoise Lite with a visual representation. This can be used for development purposes, testing noise settings and generating noise textures for export.

Source code can be found in the [WebPreviewApp](/WebPreviewApp/) directory.

![Simplex FBm](https://user-images.githubusercontent.com/1349548/275292148-242e95c7-94e7-4801-bc4a-d683a8822382.png)

## Performance Comparisons

Benchmarked using C++ version with [NoiseBenchmarking](https://github.com/Auburn/NoiseBenchmarking)

- CPU: Intel 7820X @ 4.9Ghz
- OS: Win10 x64
- Compiler: clang-cl 10.0.0 -m64 /O2

Million points of noise generated per second (higher = better)

| 3D                 | Value  | Perlin | (*Open)Simplex | Cellular |
|--------------------|--------|--------|----------------|----------|
| FastNoise Lite     | 64.13  | 47.93  | 36.83*         | 12.49    |
| FastNoise (Legacy) | 49.34  | 37.75  | 44.74          | 13.27    |
| FastNoise 2 (AVX2) | 494.49 | 261.10 | 268.44         | 52.43    |
| libnoise           |        | 27.35  |                | 0.65     |
| stb perlin         |        | 34.32  |                |          |

| 2D                 | Value  | Perlin | Simplex | Cellular |
|--------------------|--------|--------|---------|----------|
| FastNoise Lite     | 114.01 | 92.83  | 71.30   | 39.15    |
| FastNoise (Legacy) | 102.12 | 87.99  | 65.29   | 36.84    |
| FastNoise 2 (AVX2) | 776.33 | 624.27 | 466.03  | 194.30   |

## Credits:

- [OpenSimplex2](https://github.com/KdotJPG/OpenSimplex2) for the OpenSimplex2 noise algorithm
- [@KdotJPG](https://github.com/KdotJPG) for implementing all the OpenSimplex algorithms and the Java port
- [CubicNoise](https://github.com/jobtalle/CubicNoise) for the Value (Cubic) noise algorithm
- [@Rover656](https://github.com/Rover656) for creating the preview GUI and porting FastNoise Lite to C and HLSL.
- [@snowfoxsh](https://github.com/snowfoxsh) for creating the JavaScript port.
- [@dotlogix](https://github.com/dotlogix) for creating the GLSL port.
- [@ForeverZer0](https://github.com/ForeverZer0) for creating the Zig and Go ports.
- [@Keavon](https://github.com/Keavon) for creating the Rust port.
- [@jordan4ibanez](https://github.com/jordan4ibanez) for creating the Fortran port.
- [@gregoryfmartin](https://github.com/gregoryfmartin) for creating the Powershell port.
- [@itsdanott](https://github.com/itsdanott) for creating the Odin port.
- [@Zylann](https://github.com/Zylann) for creating the Haxe port.
- [@CptnRoughnight](https://github.com/CptnRoughnight) for creating the Pascal port.
- [@Tinkerer_Red]([https://github.com/CptnRoughnight](https://github.com/tinkerer-red)) for creating the GameMaker port.

## Contributing

New ports of FastNoise Lite are always welcome, create a PR or come discuss the port with me on the discord linked above.
I'm not an expert or even familiar with every language FastNoise lite has been ported to, so if you see something that could be improved please contribute or create a GitHub issue.


# Examples

![Ridged Fractal](https://user-images.githubusercontent.com/1349548/275292765-498f804b-96f8-4187-860f-7d6c49f6fc88.png)

![Cellular](https://user-images.githubusercontent.com/1349548/275292225-4e5a0379-834d-4e6e-ab2d-2c0e8e2ee209.png)

![Cellular Fractal](https://user-images.githubusercontent.com/1349548/275292294-ebb3bb00-757f-46c3-9e18-3bdc73f96719.png)

![Cellular Value Warped](https://user-images.githubusercontent.com/1349548/275292149-42a42aa7-d1b1-4c2f-856f-02fd80e84c78.png)

![Value Warped](https://user-images.githubusercontent.com/1349548/275293046-724b3aa4-1a6f-4b08-b421-8d32b6a69311.png)
