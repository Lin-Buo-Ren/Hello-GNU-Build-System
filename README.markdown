# Hello GNU Build System
This is a starter project for learning GNU Build System and its features and constraints.  
&lt;<https://github.com/Lin-Buo-Ren/Hello-GNU-Build-System>&gt;  
[![Build Status of the latest snapshot on Travis CI](https://travis-ci.org/Lin-Buo-Ren/Hello-GNU-Build-System.svg?branch=master)](https://travis-ci.org/Lin-Buo-Ren/Hello-GNU-Build-System)

## License
This intellectual property is licensed under GNU Generic Public License version 3, and other recent versions you like.

## Obstacles For Projects To Adopt The GNU Build System
### Doesn't Support Source Code Filename With Spaces
#### Configurations That Will Trigger This Issue
* /home/user/projects/my-project/src/Hello World.c

#### Explanation
Although the manual doesn't quite clearly point out, GNU Make(and thus, Automake and Autoconf etc.) doesn't really compatible with filenames with space character(s) due to space been specify as the filename separator.

#### Workaround
Don't use source filenames with spaces.

#### References
* GNU Automake Manual - FAQ - Limitations on File Names  
	```
		Portable packages should limit themselves to POSIX file names. These can contain ASCII letters and digits, ‘_’, ‘.’, and ‘-’. File names consist of components separated by ‘/’. File name components cannot begin with ‘-’.
	```

	```
		Source and installation file names like main.c are limited even further: they should conform to the POSIX/XOPEN rules described above.
	```

* [GNU Make meets file names with spaces in them | CMCrossroads](https://www.cmcrossroads.com/article/gnu-make-meets-file-names-spaces-them)
* [shell - Can GNU make handle filenames with spaces? - Stack Overflow](https://stackoverflow.com/questions/9838384/can-gnu-make-handle-filenames-with-spaces#9838604)

While there *are* workarounds but it is still too fragile to deal with not even thinking about Automake and it's friends.

### Doesn't Support Source Tree Directoryname With Spaces
Although the manual doesn't quite clearly point out, GNU Build System doesn't really compatible with directorynames with space character(s).

#### Configurations That Will Trigger The Issue
* /home/user/projects/my-project/Source Code/main.c

#### References
* [Re: should a space really be a "special character" ?](https://lists.gnu.org/archive/html/autoconf/2005-07/msg00014.html)

	> -** The configure command now diagnoses attempts to use a working or source
	> -  directory whose name contains a special character like space, newline, or "\".
	> -  Such names are not supported, and can cause "configure" to crash.

## Some Compability Issues Need To Keep In Mind Of
### Built Aritfacts Filename With Hyphens In Makefile.am
Hyphens needs to be escaped as underscores in Makefile.am