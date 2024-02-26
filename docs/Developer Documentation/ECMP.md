# ECMP Files

## What are .ecmp files?

.ecmp files are used to create packages that are installed using [CCCP](http://github.com/Soviet-Linux/CCCP) and [libspm](https://github.com/Soviet-Linux/libspm).

## Structure

.ecmp files use a [toml](https://toml.io) like syntax to identify themselves.

Example of an .ecmp file:

```toml
[info] 
name = example
version = 1.0.0
type = src 
license = Example
url = example.com 
sha256 = sha256 

[description] 
Example

[dependencies]
exampledep

[makedependencies]
examplebuilddep

[download]
wget $URL
tar -xzf "file" 

[install] 
make $MAKE_FLAGS
make DESTDIR=$BUILD_ROOT install

[special]
echo "This is SPECIAL"
```

You can see more files in the [OUR Repo](https://github.com/Soviet-Linux/OUR)

### Parts of an .ecmp file

An .ecmp is split into 7 parts each with their own purpose or step on installing a package

#### `[info]` Section

This section contains information about the package and has 6 subparts which are not all required  \
(Section **Required**)

- `name` The package name same as the package filename (**Required**)
- `version` The package version (**Required**)
- `type` The way the package is installed like is it compiled the its src is it a binary then its bin (**Required**)
- `url` The package download URL (**Required**)
- `sha256` The SHA-256 hash of the downloaded file from `url` section (**Required**)
- `license` The license of the package (**Not Required**)

#### `[description]` Section

This section contains a description of the package also markdown is supported on this section  \
(Section **Not Required**)

#### `[download]` Section

This section contains the download command for the package  \
(Section **Required**)

#### `[dependencies]` Section

This section contains a list of dependencies needed by a package (Add Multiple dependencies by adding a newline between the dependencies)  \
(This Section **is required depending on the package**)

#### `[makedeps]` Section

This section contains a list of the dependencies needed by the package at compile time (Add multiple dependencies by adding a newline between the dependencies)  \
(This Section **is required depending on the package**)

#### `[install]` Section

This section is basically a [bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) script that will install the package by the commands you provide  \
(**Required**)

#### `[special]` Section

This section is a [bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) script that runs after the installation of a package  \
(**Not Required**)

## Important info about the .ecmp files

The .ecmp has some environment variables that can be used through out the .ecmp file here is a list of the available variables:

1. $NAME Variable
This Variable contains the package name (The name is get by the [`[info]` Section](#info-section))

2. $VERSION Variable
This Variable contains the package version (The version is get by the [`[info]` Section](#info-section))

3. $URL Variable
This Variable contains the package URL (The URL is get by the [`[info]` Section](#info-section))

5. $BUILD_ROOT Variable
This Variable contains a fake installation directory given by [CCCP](https://github.com/Soviet-Linux/CCCP) and [libspm](https://github.com/Soviet-Linux/libspm)


