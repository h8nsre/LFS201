# Chapter 1 Introduction - Notes

## 1.3 Introduction
Course primarily designed for *system administrators*.

Tasks you need/want to do: configuring, running, troubleshooting multiple machines in Enterprise environment

Want to learn how to do things properly and natively in Linux

Course **not** designed primarily for:
1. New users without much experience with *any* operating system
2. Kernel or application developers
3. Experienced administrators concentrating on performance tuning

If 1, take LFS101x - Introduction to Linux (found on [edX](https://www.edx.org/course/introduction-to-linux))

If 2, may find material interesting, especially if you have more knowledge regarding:
- operating system theory
- kernel internals
- applications

The more you know about above, the more you will get from course.

If 3, will be skimmed in course, but take more advanced courses dedicated to performance tuning, such as LFS426.


## 1.4 Relationship to LFS101x
Assumption: You've taken [LFS101x](https://www.edx.org/course/introduction-to-linux), or have equivalent or better knowledge than gained from course.

Recommendation: sign up, or at least do a quick browse through material. It's free!

Some content areas covered in LFS101x covered in LFS201, but at greater detail. Eg. package management

Other topics necessary for system administrators, but not covered in course:
- text editors (vi, emacs, nano, gedit, etc.)
- finding Linux documentation (getting help)
- Manipulating text (sed, grep, awk, cut, paste, tail, head, etc.)
- file utilities (find, locate, file, etc.)
- printing (configuring printers, managing print jobs)
- graphical interfaces and their administration
- bach shell scripting
- system installation

Strong recommendation: at least take a look at LFS101x. If not completely familiar with some basic utilities and procedures used in LFS201, can probably find in LFS101x.


## 1.5 Course Formatting
Various types of content contained in course, and color coding and formats used to distinguish them:
- **Bold: names of programs or services (or used for emphasis)**
- Light blue: hyperlinks
- Dark blue: text typed at the command line
- Green: system output at the command line
- Brown: files names and file content

(Will come back to add actual color to text after learning more about Markdown styles)

## 1.13 Read the Documentation
After discussion of crafting command using Linux utility program, may only show one or few examples of choice or argument, options, etc. May also not consider less common modes of usage -> many programs *incredibly* versatile and have many rarely-used features.

May **explicitly** say "read the **man** page for more detail" from time to time, but assume that it is **implicitly** stated all the time. Must develop habit of reading easily access documentation for your Linux distribution without prompting, for all but simplest utilities.

Besides **man**, most utility programs also have built-in help and usage information: usually access by using **--help** option, eg. **df --help**.


## 1.14 Target Platform
Course designed to work on x86-based platforms, either on native hardware or running as **virtual machine (VM)**. Almost everything also relevant for othr architectures, but real or virtual x86 cover majority of deployments.

No consideration of 32-bit; assume 64-bit throughout. If running 32-bit x86, mostly everything will still be valid, although not tested by course.

Also *not* targeting **embedded Linux** platforms. Although deployments based on same Linux kernel and use many same user space ingredients, usually no talk about system administration for devices used as appliances. Has important basic ingredients that are very quite different, eg. using different boot loader programs and filesystems. Resources, eg. memory, processor power, and storage capacity, also differ greatly.

Same considerations apply to Android (particular form of embedded Linux). While kernel is still Linux, filesystem and application space extremely different from what is found on standard Linux systems.


## 1.15 Command Line vs. Graphical Interface
Many administrative tasks can be accomplished either from command line or from within graphical application. More flexibility and additional capability in command line approach (no indirection layer). Drawback for command line: administrator may have more to remember or need to look up info when task needs to be accomplished.

Variety of graphical desktop environments in Linux. Two most common:
- GNOME
- KDE
Each with multiple versions (generations).

Course not involved with graphical interfaces: too much variation, many servers do not have graphical interface installed.

For course, work from command line on local machine using either console or terminal emulator such as **gnome-terminal** running on graphical desktop. Can also work remotely through **ssh** or **vpn** session. Almost everything apply equally well in remote session case, except for when physical access to machine needed, eg. booting into rescue environment.