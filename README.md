# nobuild

Header only library for writing build recipes in C.

## Main idea

The idea is that you should not need anything but a C compiler to build a C project. No make, no cmake, no shell, no cmd, no PowerShell etc. Only C compiler. So with the C compiler you bootstrap your build system and then you use the build system to build everything else.

Try it out right here:

```
$ cc ./nobuild.c -o nobuild
$ ./nobuild
```

Explore [nobuild.c](./nobuild.c) file and the [examples](./examples) folder to learn more.

## How to use the library in your own project

1. Copy [nobuild.h](./nobuild.h) to your project
2. Create `nobuild.c` in your project with the build recipe. See our own [nobuild.c](./nobuild.c) for an example.
3. Bootstrap the `nobuild` executable:
   - `$ cc nobuild.c -o nobuild` on POSIX systems
   - `$ cl.exe nobuild.c` on Windows with MSVC
4. Run the build: `$ ./nobuild`
