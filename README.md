# Toy Tutorial

This contains sample code to support the tutorial on using MLIR for
building a compiler for a simple Toy language.

See [docs/Tutorials/Toy](../../docs/Tutorials/Toy) at the root of
the project for more informations.

### Installing MLIR on Mac

```sh
brew install cmake ninja

git clone --depth=1 https://github.com/llvm/llvm-project.git
mkdir llvm-project/build
cd llvm-project/build

cmake -G Ninja ../llvm \
-DLLVM_ENABLE_PROJECTS=mlir \
-DLLVM_BUILD_EXAMPLES=ON \
-DLLVM_TARGETS_TO_BUILD="X86;AArch64" \
-DCMAKE_BUILD_TYPE=Release \
-DLLVM_ENABLE_ASSERTIONS=ON \
-DLLVM_ENABLE_BINDINGS=OFF

cmake --build . --target check-mlir
cmake --build . --target install
```
