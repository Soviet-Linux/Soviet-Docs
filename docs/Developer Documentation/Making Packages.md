# Making Packages for Soviet-Linux

Making packages for [OUR Repository](https://github.com/Soviet-Linux/OUR) is highly apreciated look below to see details on how to make them

## Details about packages

Every package is made using the [.ecmp file format](ecmp.md)

## Making a Package

You can create a package with two diffrent ways

### Using the mkspm program

This is recommended because its more easier to make them this way  \
[mkspm](https://github.com/Soviet-Linux/spm-utils/blob/main/mkspm) is a python file that is a part of [spm-utils](https://github.com/Soviet-Linux/spm-utils/) and can be obatianed by downloading [this](https://raw.githubusercontent.com/Soviet-Linux/spm-utils/main/mkspm)

1. Download [mkspm](https://github.com/Soviet-Linux/spm-utils/blob/main/mkspm)
2. Run ```mkspm```
When you run ```mkspm``` you should also put the package name followed by a url to where you download the package from so the full command should look like this:

``mkspm nameofthepackage urltowhereyoudownloadthepackage``

3. Make Some Changes
When you run ```mkspm``` it creates an template .ecmp file meaning that the files needs to be edited so it can be a valid file you should see the [.ecmp file format documentation](ecmp.md)

### Making it from scratch 

To make an .ecmp file from scratch you should see the [.ecmp file format documentation](ecmp.md)
this should help you build a package file

## Testing a package file

This is an essentiall step when you want to make a package so you are sure that package actually works properly  \
To do this you need [spm-test](https://github.com/Soviet-Linux/spm-utils/blob/main/spm-test) from [spm-utils](https://github.com/Soviet-Linux/spm-utils/)

After getting [spm-test](https://github.com/Soviet-Linux/spm-utils/blob/main/spm-test) from [spm-utils](https://github.com/Soviet-Linux/spm-utils/) just run: ``spm-test packagefilename``

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
    git add file
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
