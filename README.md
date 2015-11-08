<img
  src="/img/bash-shellshock.png"
  width="100"
  align="right"
/>

# Useful Unix Commands
You can also read the [Portuguese](translation/README.pt-br.md).

## About it
> If you're starting with bash commands and aren't so familiar with some of them, this repository aims to help you. If you know a command that is not here or think that something can be better explained feel free to fork and make a pull request. *

## Table of Contents
* [Home Directory Shortcut](#home-directory-shortcut)
* [Present Working Directory](#present-working-directory)
* [Listing Files](#listing-files)
* [Link](#link-ln)

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
ls [options] [names]
```

And you can get the list of options [here](http://www.techonthenet.com/unix/basic/ls.php)

#### Link (ln)
One terrific command that is extremely useful in settings environments is the <i>ln</i>. It creates links to files or folders in order to avoid duplication of resources in the file system. A great example is the deployment of an application to a webserver folder. Instead of copying the folder from the workspace to the webserver, a link can solve this problem without duplication. There are two types of links: Hard Links and Symbolic Links

##### Hard Links
Hard Link is the default option for the <i>ln</i> command. It creates a physical and identical copy of the linked resource in the disk. Everytime the source changes, his copy changes too. Notice that in case of deletion of the source, the copied resource still living as an independent file. In the following example, a folder called <i>copiedResources</i> is created in the current folder with the same content of <i>bin/resources</i>

```sh
ln bin/resources copiedResources
```

##### Symbolic Links
