<img
  src="/img/bash-shellshock.png"
  width="100"
  align="right"
/>

# Useful Unix Commands
You can also read the [Portuguese](translation/README.pt-br.md) version.

## About it
> If you're starting with bash commands and aren't so familiar with some of them, this repository aims to help you. If you know a command that is not here or think that something can be better explained feel free to fork and make a pull request. *

## Table of Contents
* [Home Directory Shortcut (~)](#home-directory-shortcut-)
* [Present Working Directory (pwd)](#present-working-directory-pwd)
* [Listing Files (ls)](#listing-files-ls)
* [Link (ln)](#link-ln)
* [Creating Directories (mkdir)](#creating-directories-mkdir)
* [Copying files and directories (cp)]()

#### Home Directory Shortcut (~)
In Unix systems, you can reference your home directory from anywhere you're located just typing the tilde(~) character. If you try ~ in terminal, you get the following message:

```sh
$ ~
-bash: /Users/rafaelcfreire: is a directory
```

#### Present Working Directory (pwd)
This command prints where you are at any moment in your file system. Go to a specific folder and type <i>pwd</i> in your terminal:

```sh
$ pwd
/Users/rafaelcfreire/github/unix-commands
```

#### Listing Files (ls)
The <i>ls</i> command show the files and directories that are under your current directory by default, if you want to see from different directories just specify it address as shown next. 

List the current directory
```sh
$ ls
```

List the <i>files</i> directory
```sh
$ ls /home/personal/files
```

The sintax of the <i>ls</i> command is:

```sh
$ ls [options] [names]
```

And you can get the list of options [here](http://www.techonthenet.com/unix/basic/ls.php)

#### Link (ln)
It creates links to files or folders in order to avoid duplication of resources in the file system. There are two types of links: Hard Links and Symbolic Links

##### Hard Link
Hard Link is the default option for the <i>ln</i> command and it works only for files, not directories. It creates a physical and identical copy of the linked resource in the disk. Everytime the source changes, his copy changes too. Notice that in case of deletion of the source, the copied resource still living as an independent file. In the following example, a file called <i>localReadMe.md</i> is created in the current folder with the same content of <i>bin/resources/README.md</i>

```sh
$ ln bin/resources/README.md localReadMe.md
```

##### Symbolic Links
Considering that hard link does not work for directories, you should use symbolic links for that operation. To create a symbolic link to a directory, we can use the -s flag. This can also be used for linking to files as well, not just directories.
Symbolic links can also link to files or directories on other file systems. This makes symbolic links (symlinks) more powerful, and more common than the default hard links.

```sh
$ ln -s bin/resources copy
```

#### Creating Directories (mkdir)
This command is used to create directories, if the flag <i>-p</i> is used you can create nested directories.

```sh
$ mkdir -p test/nested
```

#### Copying files and directories (cp)
