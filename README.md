# Custom Clang for Xcode
I've configured this Xcode plugin to point to a custom version of Clang built from the source control version ("HEAD").

The path to my clang install is hard-coded in [Contents/Resources/Clang-Head.xcspec](Contents/Resources/Clang-Head.xcspec):

    ExecPath = "/opt/llvm-head/bin/clang";

You may need to change this to point to wherever you've installed your own version of Clang.

## Installation

```bash
# Create the plugins directory if it doesn't exist:
mkdir -p "~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/"
# Clone this plugin directly into that directory:
git clone git@github.com:bholt/Clang-Head.xcplugin "~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/Clang-Head.xcplugin"
```

## Using from CMake:

```cmake
set(CMAKE_XCODE_ATTRIBUTE_GCC_VERSION "com.apple.compilers.clang.3_4")
```
