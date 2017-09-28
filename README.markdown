# Hello GNU Build System
This is a starter project for learning GNU Build System and its features and constraints.  
&lt;<https://github.com/Lin-Buo-Ren/Hello-GNU-Build-System>&gt;

## License
This intellectual property is licensed under GNU Generic Public License version 3, and other recent versions you like.

## Obstacles For Projects To Adopt The GNU Build System
### Source Code Filename With Spaces
Although the manual doesn't quite clearly point out, GNU Make doesn't really compatible with filenames with space character(s).  The following is a few location that mentions this issue:

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