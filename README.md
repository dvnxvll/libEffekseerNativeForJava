# libEffekseerNativeForJava

This is primarily a repo to allow me to build the shared library `libEffekseerNativeForJava.so` for in use with [ChloePrime/AAAParticles](https://github.com/ChloePrime/AAAParticles).

This repo used modified, updated code from:
[effekseer/EffekseerForMultiLanguages](https://github.com/effekseer/EffekseerForMultiLanguages)

Changes included in inital commit:
- Removed swig wrapper script, used built-in CMake Swig wrapper.
- Fixed include directives to point to correct Effekseer headers
- stripped Swig build to only build for java, as this is only for Minecraft builds.

To Build:
```bash
git clone https://github.com/dvnxvll/libEffekseerNativeForJava.git

cd libEffekseerNativeForJava

git submodule update --init

cmake -B build -DCMAKE_POLICY_VERSION_MINIMUM=3.5

cmake --build build
```

`libEffekseerNativeForJava.so` Will be in `build/src/Core/libEffekseerNativeForJava.so`

To Install:
Copy `libEffekseerNativeForJava.so` to your instances minecraft folder. Eg:
`cp build/src/Core/libEffekseerNativeForJava.so $HOME/.monolith/instances/"NeoForge 1.21.1"/`
