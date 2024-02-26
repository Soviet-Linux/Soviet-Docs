# CCCP

## What is CCCP

[CCCP](https://github.com/Soviet-Linux/CCCP) is our custom package manager build in [The C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language)) 
and it is desinged to make your life easier dealing with packages using the [OUR package repository](https://github.com/Soviet-Linux/OUR).

## How to use CCCP

[CCCP](https://github.com/Soviet-Linux/CCCP) is a command line tool, so you need to know how to use the terminal to use it. Don't worry it's not that bad since we designed 
it to be as simple as possible.

### Commands

- Everyday Options:
    - `-h` or `--help` this prints a help message
    - `-v` or `--version` this prints the version of the package manager
    - `-i` or `--install` followed by the package name this installs a package from OUR repo
    - `-r` or `--remove` followed by the package name this removes a package from the system
    - `-l` or `--list` this lists all the packages that are installed in your system
    - `-s` or `--search` followed by the package name/query to find a package
    - `--update` checks for any updates in your system
    - `--upgrade` upgrades all the packages that are installed in your system

- Advanced Options:
    -  `-Yy` or `-Nn` to automatically accept or decline the prompts acordingly
    -  `--no-checksum` to skip the checksum verification
    -  `-ow` or `--overwrite` this overwrites installed packages
    -  `-dbg` or `--debug` followed by a number from 0 to 4 to indicate the debug level
    -  `--verbose` this swtiches to verbose output
    -  `-pkg` or `--package` followed by a path to an [.ecmp file](../Developer%20Documentation/Making Packages.md) to install directly from the file

*Advanced Options should only be used if you know what you are doing*
