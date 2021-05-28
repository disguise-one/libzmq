```
mkdir build
cd build
cmake.exe .. -DWITH_LIBSODIUM=ON -DSODIUM_INCLUDE_DIRS=..\\..\\libsodium\\src\\libsodium\\include -DSODIUM_LIBRARIES=..\\..\\libsodium\\bin\\x64\\Release\\v142\\dynamic\\libsodium.lib -DZMQ_MSVC_SHORT_LIB_NAMES=1
```
You may need to escape the backslashes depending on your terminal.

Open the generated solution in VS and build libzmq in Release and Debug.
Copy the built files from `build/bin` *and* `build/lib` to match this tree:
```
bin
└── x64
    ├── Debug
    │   └── v142
    │       └── dynamic
    │           ├── libzmq.dll
    │           ├── libzmq.exp
    │           ├── libzmq.ilk
    │           ├── libzmq.lib
    │           └── libzmq.pdb
    └── Release
        └── v142
            └── dynamic
                ├── libzmq.dll
                ├── libzmq.exp
                └── libzmq.lib
```
Now follow the conan guide.

