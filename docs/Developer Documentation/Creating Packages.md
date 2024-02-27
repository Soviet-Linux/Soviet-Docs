# Creating Packages for Soviet-Linux

Creating packages for [OUR Repository](https://github.com/Soviet-Linux/OUR) is highly appreciated. Below are the details on how to create them.

## Details about Packages

Each package is created using the [.ecmp file format](ECMP.md).

## Creating a Package

There are two different ways to create a package.

### Using the mkspm Program

This method is recommended as it is easier. [mkspm](https://github.com/Soviet-Linux/spm-utils/blob/main/mkspm) is a Python file that is part of [spm-utils](https://github.com/Soviet-Linux/spm-utils/). It can be obtained by downloading [this](https://raw.githubusercontent.com/Soviet-Linux/spm-utils/main/mkspm).

1. Download [mkspm](https://github.com/Soviet-Linux/spm-utils/blob/main/mkspm).
2. Generate a template ecmp.
When you run `mkspm`, you should also provide the package name followed by a URL from where you can download the package. The full command should look like this:

``mkspm nameofthepackage urltowhereyoudownloadthepackage``

For example: 
`mkspm bash https://ftp.gnu.org/gnu/bash/bash-5.2.9.tar.gz`

3. Make Some Changes
When you run ```mkspm``` it creates a template .ecmp file, meaning that the file needs to be edited to be a valid file. For more information, see the [.ecmp file format documentation](ECMP.md).

### Making it from scratch 

To make an .ecmp file from scratch, see the [.ecmp file format documentation](ECMP.md). This should help you build a package file.
## Testing a Package File

This is an essential step when you want to make a package, to ensure that the package actually works properly. To do this, you need [spm-test](https://github.com/Soviet-Linux/spm-utils/blob/main/spm-test) from [spm-utils](https://github.com/Soviet-Linux/spm-utils/).

You can test a package by running:
```
spm-test <package file>
```
## Commiting and Contributing to OUR

### Prequisites

- [Github Account](https://github.com/)
- [Git](https://git-scm.com/) or any other git client
- Basic knowledge of git

### Contributing

1. Fork the repository
2. Clone your fork:  \
    To clone your fork you can use:

    ```
    git clone linktoyourrepo
    ```

3. Make your changes (recommended make a new branch when making changes)
4. Rebuild the database using ```./mkall```
5. Commit your changes:  \
    To commit your changes you need to stage them you can do this by running:
> Note: You must Stage the all.db after rebuilding the database

    ```
    git add <file>
    ```

    Or for every every file you changed:

    ```
    git add -A
    ```

    Then to commit the changes(it is preffered to sign the commit so they are verified you can visit [this](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits) for more information)
    
    Without signing:

    ```
    git commit 
    ```

    Signing:

    ```
    git commit -S
    ```

6. Push your changes:  \
    To push your changes use:

    ```
    git push
    ```

7. Open PR(Pull Request)


