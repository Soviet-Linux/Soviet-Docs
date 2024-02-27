# CCCP

## What is CCCP

[CCCP](https://github.com/Soviet-Linux/CCCP) is our custom package manager built in [The C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language)). 
It is designed to simplify your interaction with packages using the [OUR package repository](https://github.com/Soviet-Linux/OUR).

## How to use CCCP

[CCCP](https://github.com/Soviet-Linux/CCCP) is a command line tool, so you need to be familiar with the terminal to use it. We've designed 
it to be as user-friendly as possible.

### Commands

- Everyday Options:
    - `-h` or `--help`: Prints a help message
    - `-v` or `--version`: Prints the version of the package manager
    - `-i` or `--install` followed by the package name: Installs a package from OUR repo
    - `-r` or `--remove` followed by the package name: Removes a package from the system
    - `-l` or `--list`: Lists all the packages that are installed on your system
    - `-s` or `--search` followed by the package name/query: Finds a package
    - `--update`: Checks for any updates in your system
    - `--upgrade`: Upgrades all the packages that are installed in your system

- Advanced Options:
    -  `-Yy` or `-Nn`: Automatically accept or decline the prompts accordingly
    -  `--no-checksum`: Skips the checksum verification
    -  `-ow` or `--overwrite`: Overwrites installed packages
    -  `-dbg` or `--debug` followed by a number from 0 to 4: Indicates the debug level
    -  `--verbose`: Switches to verbose output
    -  `-pkg` or `--package` followed by a path to an [.ecmp file](../Developer Documentation/Creating Packages.md): Installs directly from the file

*Advanced Options should only be used if you know what you are doing*
