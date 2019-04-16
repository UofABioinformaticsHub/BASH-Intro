* TOC
{:toc}

# Introduction

[Opening Presentation](https://gitpitch.com/UofABioinformaticsHub/BASH-Intro/)

## General Information

Thank you for your attendance and welcome to the *Introduction to Bash: Using the Terminal For Bioinformatics* Workshop.
This is series of training workshops and materials developed by the Bioinformatics Interest Group - South Australia (BIG-SA), specifically using the skills and resources of the Bioinformatics Hub (University of Adelaide) and the ACRF Cancer Genomics Facility (UniSA).

Some additional resources run by the Bioinformatics Hub which may be of interest beyond today are:

- A [University web-page](http://www.adelaide.edu.au/bioinformatics-hub/)
- To be kept up to date on upcoming events and workshops, please join the internal [Bioinformatics mailing list](http://list.adelaide.edu.au/mailman/listinfo/bioinfo)
- A [Twitter account](https://twitter.com/UofABioinfoHub/)
- An active Slack team for discussing Bioinformatics questions with the local community. Slack teams do require an invitation to join, so please [email the Hub](mailto:bioinf_hub@adelaide.edu.au) to join the community. All are welcome.

## Computer Setup

For all sessions, we'll be running on virtual machines (VMs) and we'd like you to log in to these machines using a terminal.
This is how we commonly interact with these machines so will be good practice.
If you're on macOS or Ubuntu, you simply need to know how to find a terminal:

- macOS: <kbd>⌘</kbd>+<kbd>Space</kbd> then type the word terminal
- Ubuntu: <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>T</kbd>

For **Windows users**, we advise either using `PuTTY` or `git bash`, both of which require installation.
Installation instructions [can be found here](../install/windowsInstall.md).
If you don't have adminstrative access and require help from ITS, please call them and ask for PuTTY to be installed as this is very common within the University.
Otherwise `git bash` is the preferred option.
Once you've got this setup, open `git bash` and you should see something that looks like a terminal.

Most of the tools we use on the VM are also available in your macOS terminal, or in `git bash`.
There can be subtle differences in the way they work, but by and large with both of these you can actually run `bash` on your own machine as well as the remote VM we connect to.


## Logging Onto Your VM

You will have been assigned an IP address which corresponds to your VM, and we will connect to this using your terminal.
Enter the command

```
ssh trainee@<your.ip.address>
```

Type `yes` when requested and **use the password** provided.
At this point you should see a message similar to:

```
Welcome to Ubuntu 16.04.5 LTS (GNU/Linux 4.4.0-116-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

117 packages can be updated.
46 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

```

Your terminal will also now have the value `trainee@fib_2019-xxx:~$` at the far left and this is your machine identifier.
It's mostly irrelevant information for you, but is just a check that you're in the correct place.

### Note for PuTTY users

The login is slightly different when using PuTTY, and you will enter `trainee@<your.ip.address>` in the main space provided (under `Host Name or IP address`) and hit `Enter` (or the `Open` button).
Beyond that, you should be able to enter your password and yuo should see the same login screen.


## Course Information

### Course Outline
{:.no_toc}

There will be a number of areas covered during these sessions:

- using the terminal/bash shell
- the linux filesystem and how to navigate around
- working with files/directories and wildcards
- common/standard linux command tools (filters)
- command line arguments and file permissions
- pipes and redirects
- regular expression
- advanced text processing tools (`grep`, `sed`)
- bash scripting

The majority of data handling and analysis required in the field of bioinformatics uses the command line, alternatively known as the terminal or the `bash` shell.
This is a text-based interface in which commands must be typed, as opposed to the Graphical User Interfaces (aka GUIs) that most of us have become accustomed to.
Being able to access these tools enables you to more fully utilise the power and capabilities of your machine, for both Linux and Mac operating systems, and to a lesser extent will even enable you to dig deeper on a Windows system.

While some of the tools we cover may appear trivial, they are used on a daily basis by those working in the field.
These basic tools are essential for writing what are known as shell scripts, which we will work towards throughout the first three sessions and begin to cover in the last.
These are essentially simple programs that utilise the inbuilt functions of the shell, and are used to automate processes such as de-multiplexing read libraries, or aligning reads to the genome.
A knowledge of this simple type of programming and navigation is also essential for accessing the high-performance computing resources such as *phoenix*.

### Course Aims
{:.no_toc}
The long-term goal of this workshop is to enable you to carry out your own data analysis in a **reproducible** manner, using standard bioinformatics tools or write your own programs.
This course serves as a prerequisite for the Introduction to Next Generation Sequencing (NGS) Data workshop coming later in the year.

By the end of both courses, we expect the participants to:
1. Be relatively comfortable working with the command line interface, and familiar with the standard Unix command line tools
2. Understand standard NGS data formats
3. Be able to run several basic NGS data analysis methods (e.g. variant calling)
4. Understand how some simple python scripts work for custom data analysis

### Acknowledgements
{:.no_toc}

This course has been put together by Paul Wang, John Toubia, Stephen Pederson and Jimmy Breen, based on previous material prepared by Stephen Bent, Nathan Watson-Haigh and Dan Kortschak.

Sections of the workshop are also based loosely on material and courses prepared
by Software Carpentary (http://software-carpentry.org/lessons/) and Ryans Tutorials
(http://ryanstutorials.net/)

We hope it will be useful in enabling you to continue and to advance your research.

## Protocols

### Entering Commands
{:.no_toc}

In the following pages, we **strongly encourage** you to manually type all commands.
The mistakes you will inevitably make will actually *be important learning steps*.
Additionally, in your work beyond today, you will probably not have any instructions to follow.
The experience of typing these commands will equip you for future work far better than if you simply copy and paste.

### Copy and Paste
{:.no_toc}

As we're dealing with a large number of setups here the strategy for copy and pasting will vary.
To paste into a standard bash terminal, you usually use <kbd>Shift</kbd>+<kbd>Ctrl</kbd>+<kbd>C</kbd> for copy, and <kbd>Shift</kbd>+<kbd>Ctrl</kbd>+<kbd>C</kbd> for paste.
On Mac this may be different, and for `git bash` and `PuTTY` this is also different.
Typing will be much simpler, and we'll show you a lot of shortcuts to speed this up.

### Differences between platforms
{:no_toc}

At various places in the notes there are comments relating to differences between commands on linux and macOS.
These will not make a difference to your work during the workshop but may help you to understand differences you see in your own work later.
When you find different uses of commands and options, read the documentation for the tool to understand the differences.


[Home](https://UofABioinformaticsHub.github.io/BASH-Intro/)
