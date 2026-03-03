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
* **Root user:** user with elevated privileges to modify files.
* **sudo**: super-user-do
* **authentication**: The process of verifying who someone is
* **authorization**: The concept of granting access to specific resources in a system

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
grep [string]
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
# displays hidden files which start with a period (.) at the beginning.
ls -a
# displays permissions to files and directories, and also other additional information, including owner name, group, file size, and last modification time.
ls -l
# displays permissions to files and directories, including hidden files. This is a combination of the other two options.
ls -la
# changes permissions on files and directories.
chmod [user_permissions], [group_permissions], [others_permissions], [document/directory]
# adds a user to the system, it can be added to a -g, default group; -G, additional group
sudo useradd [user]
sudo useradd [group] [user]
# modifies existing user accounts, to change the primary group of an existing user -g; to add supplemental group for an existing user -G
sudo usermod [group] [group_name] [user]
# changes the user’s home directory.
sudo usermod -d [directory] [user]
# changes the user’s login name.
sudo usermod -l [name] [user]
# locks the account so the user can’t log in.
sudo usermod -L [user]
# deletes a user from the system.
sudo userdel [user]
# changes ownership of a file or directory
sudo chown [user] [file/directory]
# change group owner, add ":" before group to designate it as a group name.
sudo chown :[group] [file/directory]
# display information on what other commands are and how they work
man [command]
# search for a command even if they do not know the specific command name.
apropos [word]
# search for multiple words.
apropos -a [word_1] [word_2] ... [word_n]
# displays a description of a command on a single line
whatis [command]
```

**Permissions Format**

<table><thead><tr><th width="113.79998779296875">Character</th><th width="124.20001220703125">Example</th><th>Meaning</th></tr></thead><tbody><tr><td>1st</td><td><strong>d</strong>rwxrwxrwx</td><td><p>file type : </p><ul><li>d for directory</li><li>"-" for a regular file</li></ul></td></tr><tr><td>2nd</td><td>d<strong>r</strong>wxrwxrwx</td><td><p>read permissions for user :</p><ul><li>"r" if it has read permissions</li><li>"-" if it lacks read permissions</li></ul></td></tr><tr><td>3rd</td><td>dr<strong>w</strong>xrwxrwx</td><td><p>write permissions for the user : </p><ul><li>"w" if the user has write permissions</li><li>"-" if the user lacks write permissions</li></ul></td></tr><tr><td>4th</td><td>drw<strong>x</strong>rwxrwx</td><td><p>execute permissions for the user : </p><ul><li>"x" if the user has execute permissions</li><li>"-" if the user lacks execute permissions</li></ul></td></tr><tr><td>5th</td><td>drwx<strong>r</strong>wxrwx</td><td><p>read permissions for the group : </p><ul><li>"r" if the group has read permissions</li><li>"-" if the group lacks read permission</li></ul></td></tr><tr><td>6th</td><td>drwxr<strong>w</strong>xrwx</td><td><p>write permissions for the group : </p><ul><li>"w" if the group has write permissions</li><li>"-" if the group lacks write permission</li></ul></td></tr><tr><td>7th</td><td>drwx<strong>r</strong>w<strong>x</strong>rwx</td><td><p>execute permissions for the group : </p><ul><li>"x" if the group has execute permissions</li><li>"-" if the group lacks execute permissions</li></ul></td></tr><tr><td>8th</td><td>drwxrwx<strong>r</strong>wx</td><td><p>read permissions for other : </p><ul><li>"r" if the other owner type has read permissions</li><li>"-" if the other owner type lacks read permissions</li></ul></td></tr><tr><td>9th</td><td>drwxrwxr<strong>w</strong>x</td><td><p>write permissions for other :</p><ul><li>"w" if the other owner type has write permissions</li><li>"-" if the other owner type lacks write permissions</li></ul></td></tr><tr><td>10th</td><td>drwxrwxrw<strong>x</strong></td><td><p>execute permissions for other :</p><ul><li>"x" if the other owner type has execute permissions</li><li>"-" if the other owner type lacks execute permissions</li></ul></td></tr></tbody></table>

**Chmod permissions format: \[u/g/o]\[+/-/=]\[permissions]**

<table><thead><tr><th width="113.99993896484375">Character</th><th>Description</th></tr></thead><tbody><tr><td>u</td><td>indicates changes will be made to user permissions</td></tr><tr><td>g</td><td>indicates changes will be made to group permissions</td></tr><tr><td>o</td><td>indicates changes will be made to other permissions</td></tr><tr><td>+</td><td>adds permissions to the user, group, or other</td></tr><tr><td>-</td><td>removes permissions from the user, group, or other</td></tr><tr><td>=</td><td>assigns permissions for the user, group, or other</td></tr></tbody></table>

### 1.4 Databases and SQL

* **SQL (Structured Query Language):** programming language used to create, interact and request information from a database
* **Wildcard**: is a special character that can be substituted with any other character.
* **Relational database:** A structured database containing tables that are related to each other
* **Foreign key:** column in a table that is a primary key in another table

```sql
--- display the whole table 
SELECT * FROM [table]
--- display the columns
SELECT [column_1], [column_2], ... [column_n] FROM [table]
--- which table to query
FROM [table]
--- sequences the records in a ascending order by a query based on column or columns. 
ORDER BY [column_1], [column_2], ... [column_n] 
--- sequences the records in a descending order by a query based on column or columns. 
ORDER BY [column_1], [column_2], ... [column_n] DESC;
--- create a filter
SELECT [column] FROM [table] WHERE [column] = [filter_value];
---  apply wildcards to the filter
SELECT [column] FROM [table] WHERE [column] LIKE [wildcard];
--- incorporate comparison operators (<, >, <=, >=, =, !=, <>)
SELECT [column] FROM [table] WHERE [column] [operator] [filter_value];
--- filters for numbers or dates within a range
SELECT [column] FROM [table] WHERE [column] BETWEEN ['date_1'] AND ['date_2'];
--- incorporate logical operators (AND, OR, NOT)
SELECT [column] FROM [table] WHERE [column] [operator] [filter_value] [logical_operator] [column] [operator] [filter_value];
--- inner join: rows that match on a specified column
SELECT [column] FROM [table_1] INNER JOIN [table_2] ON [table_1].[column] [operator] [table_2].[column]
--- left join: returns all the records of the first table and the rows of the second table that match on a column
SELECT [column] FROM [table_1] LEFT JOIN [table_2] ON [table_1].[column] [operator] [table_2].[column]
--- right join: returns all of the records of the second table and the rows from the first table that match on a specified column. 
SELECT [column] FROM [table_1] RIGHT JOIN [table_2] ON [table_1].[column] [operator] [table_2].[column]
--- full outer join: returns all records from both tables completely merging them.
SELECT [column] FROM [table_1] FULL OUTER JOIN [table_2] ON [table_1].[column] [operator] [table_2].[column]
--- returns a single number that represents the number of rows returned from your query.
SELECT COUNT(column) FROM [table];
--- returns a single number that represents the average of the numerical data in a column.
SELECT AVG(column) FROM [table];
--- returns a single number that represents the sum of the numerical data in a column.
SELECT SUM(column) FROM [table];
```

**Wildcards applied to the string 'a' and examples:**

<table><thead><tr><th width="95.5999755859375">Pattern</th><th>Results that could be returned</th></tr></thead><tbody><tr><td>'a%'</td><td>apple123, art, a</td></tr><tr><td>'a_'</td><td>as, an, a7</td></tr><tr><td>'a__'</td><td>as, an, a7</td></tr><tr><td>'%a'</td><td>pizza, Z6ra, a</td></tr><tr><td>'_a'</td><td>ma, 1a, Ha</td></tr><tr><td>'%a%'</td><td>Again, back, a</td></tr><tr><td>'_a<em>_</em>'</td><td>Car, ban, ea7</td></tr></tbody></table>

## 2. Course 5: Assets, Threats and Vulnerabilities

### 2.1 Introduction to asset security

* **Compliance:** process of adhering to internal standards and external regulations, a way of measuring how well an organization is protecting their assets
* **Risk**: anything that can impact the confidentiality, integrity, or availability of an asset
* **Threat**: any circumstance or event that can negatively impact assets. They are commonly categorized as two types:
  * Intentional
  * Unintentional
* **Vulnerability**: weakness that can be exploited by a threat. They can be grouped into two categories:
  * Technical
  * Human
* **Risk:** anything that can impact the confidentiality, integrity, or availability of an asset. It's calculation formula is: **Likelihood x Impact = Risk**
* **Asset management:** process of tracking assets and the risks that affect them.
* **Asset:** item perceived as having value to an organization. It can be classified in:
  * _**Restricted**_ is the highest level. This category is reserved for incredibly sensitive assets,  like need-to-know information.
  * _**Confidential**_ refers to assets whose disclosure may lead to a significant negative impact on an organization.
  * _**Internal-only**_ describes assets that are available to employees and business partners.
  * _**Public**_ is the lowest level of classification. These assets have no negative consequences to the organization if they’re released.
* **Data**: information that is translated, processed, or stored by a computer
  * **Data at rest:** not currently being accessed
  * **Data in transit**: traveling from one point to another
  * **Data in use:** being accessed by one or more users
* **Cloud-based services:** a variety of on demand or web-based business solutions. There are three main categories of cloud-based services:
  * _**Software as a service (SaaS):**_ front-end applications that users access via a web browser where the service providers host, manage and maintain all of the back-end systems for those applications.
  * _**Platform as a service (PaaS):**_ back-end application development tools that clients can access online, where the cloud service providers host and maintain the back-end hardware and software that the apps use to operate
  * _**Infrastructure as a service (IaaS):**_ customers are given remote access to a range of back-end systems that are hosted by the cloud service provider, including data processing servers, storage, networking resources, and more.
* **Cloud security:** data is stored in the cloud and accessed over the internet, several challenges arise:
  * **Misconfiguration:** customers of cloud-based services are responsible for configuring their own security environment.
  * **Cloud-native breaches**: due to misconfigured services.
  * **Monitoring access** **might be difficult** depending on the client and level of service.
  * **Meeting regulatory standards** is a concern, particularly in industries that are required by law to follow specific requirements such as HIPAA, PCI DSS, and GDPR.
* **NIST Cybersecurity Framework (CSF):** voluntary framework that consists of standards, guidelines, and best practices to manage cybersecurity risk. It consists of three main components:
  * _**Core**_: set of desired cybersecurity outcomes that help organizations customize their security plan. It consists of six functions, or parts:
    * _Identify_
    * _Protect_
    * _Detect_
    * _Respond_
    * _Recover_
    * _Govern_
  * _**Tiers:**_ a way of measuring the sophistication of an organization's cybersecurity program measured on a scale of 1 to 4. Tier 1 is the lowest score, indicating that a limited set of security controls have been implemented.&#x20;
  * _**Profiles**_**:** pre-made templates that are developed by a team of industry experts, tailored to address the specific risks of an organization or industry, used to help organizations develop a baseline for their cybersecurity plans, or as a way of comparing their current cybersecurity posture to a specific industry standard.

## 2.2 Protect organizational assets

* **Principle of least privilege:** security concept in which a user is only granted the minimum level of access and authorization required to complete a task or function.
* **Data lifecycle:** has five stages. Each describe how data flows through an organization from the moment it is created until it is no longer useful:
  * _**Collect**_
  * _**Store**_
  * _**Use**_
  * _**Archive**_
  * _**Destroy**_
* **Data governance:** set of processes that define how an organization manages information. It policies commonly categorize individuals into a specific role:
  * _**Data owner:**_ the person that decides who can access, edit, use, or destroy their information.
  * _**Data custodian:**_ anyone or anything that's responsible for the safe handling, transport, and storage of information.
  * _**Data steward:**_ the person or group that maintains and implements data governance policies set by an organization.
* **PII (Personally Identifiable Information):** any information used to infer an individual's identity, refers to information that can be used to contact or locate someone.
* **PHI:** information that relates to the past, present, or future physical or mental health or condition of an individual
* **SPII (Sensitive Personally Identifiable Information):** specific type of PII that falls under stricter handling guidelines. The S stands for sensitive, meaning this is a type of personally identifiable information that should only be accessed on a need-to-know basis, such as a bank account number or login credentials.
* **Information privacy:** refers to the protection from unauthorized access and distribution of data.
* **Information security (InfoSec):** refers to the practice of keeping data in all states away from unauthorized users.
* **GDPR (General Data Protection Regulation):** set of rules and regulations developed by the European Union (EU) that puts data owners in total control of their personal information.
* **PCI DSS (Payment Card Industry Data Security Standard):** set of security standards formed by major organizations in the financial industry.
* **HIPAA (Health Insurance Portability and Accountability Act)**: a U.S. law that requires the protection of sensitive patient health information.
* **Security audit:** a review of an organization's security controls, policies, and procedures against a set of expectations.
* **Security assessment:** a check to determine how resilient current security implementations are against threats.
* **Encryption**: process of converting data from a readable format to an encoded format. There are two main types:
  * **Symmetric encryption:** is the use of a single secret key to exchange information where the sender and receiver must know the secret key to lock or unlock the cipher.
  * **Asymmetric encryption:** is the use of a public and private key pair for encryption and decryption of data. It uses two separate keys: a public key used to encrypt data, and a private key decrypts it and is only given to users with authorized access.
* **PKI (Public key infrastructure)**: encryption framework that secures the exchange of online information
* **Cipher**: algorithm that encrypts information, and they are vulnerable to brute force attacks

