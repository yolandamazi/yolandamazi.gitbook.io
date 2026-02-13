---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Google Cybersecurity Profesional Certificate

## 0. Introduction

To get hands-on experience in cybersecurity, I’ve enrolled in the Google Cybersecurity Professional Certificate. My goal is to learn the basics through this course before deepening my skills.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2026-02-10 115806.png" alt=""><figcaption></figcaption></figure>

I’ve already completed the first three courses, which are:

* Foundations of Cybersecurity
* Play It Safe: Manage Security Risks
* Connect and Protect: Networks and Network Security

For the remaining courses, I’ll keep track of my learning through the blog, documenting the notes I consider important or relevant.

## 1. Course 4: Tools of the Trade: Linux and SQL

### 1.1 Introduction to OS

* **OS (Operating System)**: the interface between the computer hardware and the user
* **Legacy Operating System**: an OS that is not up to date while is still in use from a user. Might be vulnerable to new threats
* **Basic Input/Output System (BIOS):** a microchip that contains loading instructions for the computer and is prevalent in older systems. It's activated when you boot your computer. Standard chip since 2007.
* **Unified Extensible Firmware Interface (UEFI):** a microchip that is activated when you boot your computer and contains loading instructions for the computer and replaces BIOS on more modern systems. Mostly used on new computers.
* **Bootloader**: a software program activated by the last instruction of the microchip during the computer’s boot process. It is responsible for starting the operating system.
* **Virtual Machine (VM)**: is a virtual version of a physical computer. There are machines that don’t exist physically, but operate like they do because their software simulates physical hardware.
  * Some benefits include improved _security_ due to its isolated environment, as well as increased _efficiency_, since you can streamline multiple tasks across different machines.
* **Virtualization:** process of using software to create virtual representations of various physical machines.
* **Command Line Interface (CLI)**: a user interface that uses commands to interact with the computer
* **Graphical User Interface (GUI)**: a user interface that uses icons on the screen to manage different tasks on the computer

### 1.2 The Linux OS

* **Kernel**: a component of the Linux OS that manages processes and memory. The shell processes commands and outputs the results.
* **Filesystem Hierarchy Standard (FHS):** component of the Linux OS that organizes data. It specifies the location where data is stored in the operating system.
* **Central Processing Unit (CPU):** a computer’s main processor, which is used to perform general computing tasks on a computer. It executes the instructions provided by programs, which enables these programs to run.
* **Random Access Memory (RAM):** a hardware component used for short-term memory. It’s where data is stored temporarily as you perform tasks on your computer.
* **Hard drive**: a hardware component used for long-term memory.
* **Package**: a piece of software that can be combined with other packages to form an application. It contains the files necessary for an application to be installed including dependencies, which are supplemental files used to run an application.
* **Package managers:** is a tool that helps resolve any issues with dependencies and perform other management tasks such as install, manage, and remove packages or applications.&#x20;
  * Different package managers typically use different file extensions. For example:
    * _Red Hat Package Manager (RPM)_ has files which use the .rpm file extension, such as Package-Version-Release\_Architecture.rpm.
    * _Debian-derived_ Linux distributions, such as dpkg, have files which use the .deb file extension, such as Package\_Version-Release\_Architecture.deb.
* **Advanced Package Tool (APT)  :** a tool used with Debian-derived distributions. It is run from the command line interface to manage, search, and install packages.
* **Yellowdog Updater Modified (YUM)**  : a tool used with Red Hat derived distributions. It is run from the command line interface to manage, search, and install packages and it works with .rpm files.
* **Shell:** is the command-line interpreter that processes commands and outputs the results. It´s able to return an output or an error message
  * Different types:
    * _Bourne-Again Shell (bash)_: is the default shell in most Linux distributions since it is considered a user-friendly shell.
    * _C Shell (csh)_
    * _Korn Shell (ksh)_
    * _Enhanced C shell (tcsh)_
    * _Z Shell (zsh)_
* **Standard error:** error messages returned by the OS through the shell. Information returned by the OS through the shell is standard output.
* **Standard input:** sent to the operating system.
* **Standard output:** sent from the operating system.

**Commands learned:**

```bash
# ensure APT is installed
apt
# install/remove an app, sudo is required for elevated privileges 
sudo apt install [app_name]
sudo apt remove [app_name]
# verify [app_name] has been installed/uninstalled
[app_name]
# list all installed applications
apt list --installed
# generate output command
echo
# generate output command
expr
# clear the Bash shell command
clear
```

### 1.3 Linux commands in the bash shell

* **Root directory:** the highest-level directory in Linux, and it’s always represented with a forward slash (/).
* **Standard FHS directories:**  &#x20;directories directly below the root directory
  * /home
  * /bin: stands for “binary” and contains binary files and other executables.&#x20;
  * /etc: stores the system’s configuration files.
  * /tmp: stores many temporary files.&#x20;
  * /mnt: stands for “mount” and stores media.
* **Executables**: files that contain a series of commands a computer needs to follow to run programs and perform other functions.

```bash
# display names of files and directories in the current working directory
ls
# returns the directory that you’re currently in
pwd
# navigates between directories
cd
# displays the content of a file
cat
# displays just the beginning of a file, by default 10 lines
head
# change the number of lines returned, specify the number of lines by including -n
head -n [num_lines] [doc_name]
# display just the end of a file, by default 10 lines
tail
# returns the content of a file one page at a time
less
# searches a file and returns all lines in the file containing a string or text
grep
# sends the standard output of a command as standard input to another command
[ouput] | [input]
# search for files and directories that contain a string in the name, are a file size, or were last modified within a certain time
find
# specify the string you’re searching for
find [directory/file] -name "[string]"
find [directory/file] -iname "[string]"
# search files or directories last modified within a certain time frame based on days
find [directory/file] -mtime [-/+ days] 
# create a new file
touch [file]
# creates a new directory
mkdir [directory]
# removes, or deletes, a directory
rmdir [directory]
# removes, or deletes, a file 
rm [file]
# moves a file or directory to a new location and also to rename files
mv [directory/file] [directory]
mv [file_name] [file_name] 
# copy a file to a directory
cp [file] [directory]
# open an existing file or create a new file (ctrl + o & ctrl + x to save)
nano [file]
# overwrites your file, if does not exist it creates it
echo [string] > [file]
# >> adds your content to the end of a file
echo [string] >> [file]

```

### 1.4 Databases and SQL



