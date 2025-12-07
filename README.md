# GCC Debug
cmake --preset=gcc-debug
cmake --build --preset=gcc-debug-build

# GCC Release
cmake --preset=gcc-release
cmake --build --preset=gcc-release-build

# Clang Debug
cmake --preset=clang-debug
cmake --build --preset=clang-debug-build

# Clang Release
cmake --preset=clang-release
cmake --build --preset=clang-release-build

# Clang with ASan + UBSan
cmake --preset=clang-asan-ubsan
cmake --build --preset=clang-asan-ubsan-build
