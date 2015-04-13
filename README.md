# Mustache

C++11 header-only [Mustache](http://mustache.github.io) templates with no dependencies.

## Example

    Mustache::Mustache<std::string> tmpl("Hello {{what}}!");
    Mustache::Data<std::string> data("what", "World");
    std::cout << tmpl.render(data) << std::endl;
    // Hello World!

## Compilers Tested

- Xcode 6.3 (Clang 3.6)
- GCC 4.8
- Clang 3.4
- Visual Studio 2013

## Run Tests

For Linux and OS X:

    make

For Visual Studio 2013 (CMake 2.8+ required) open a Visual Studio Command Prompt, then:

    cmake .
    cmake --build
    Debug\mustache.exe

## TODO

- {{.}} syntax for lists of strings
- Partials?
- Lambdas?
- Visual Studio makefile
- Test against [spec](https://github.com/mustache/spec)
