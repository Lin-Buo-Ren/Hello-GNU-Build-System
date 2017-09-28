# Main Configuration File For The GNU Build System
# This file is read by both ‘autoconf’ (to create ‘configure’) and ‘automake’ (to create the various ‘Makefile.in’s).  It contains a series of M4 macros that will be expanded as shell code to finally form the ‘configure’ script.
#
# The macros prefixed with ‘AC_’ are Autoconf macros, documented in the Autoconf manual.  The macros that start with ‘AM_’ are Automake macros, documented in the Automake manual.
#
# Documentation:
#
#   * GNU Autoconf Manual
#   * GNU Automake Manual (optional)
#   * texinfo: (autoconf)Autoconf Macro Index
#   * texinfo: (automake)Macro Index
## Initialize Autoconf
AC_INIT([Hello GNU Build System], [0.0.1], [https://github.com/Lin-Buo-Ren/Hello-GNU-Build-System/issues])

## Initialize Automake
AM_INIT_AUTOMAKE([-Wall -Werror foreign])

## Let ‘configure’ script to search for a C compiler and define the variable ‘CC’ with its name
AC_PROG_CC

## The ‘AC_CONFIG_FILES’ macro declares the list of files that ‘configure’ should create from their ‘*.in’ templates.  Automake also scans this list to find the ‘Makefile.am’ files it must process
AC_CONFIG_FILES([
	Makefile
	Source_Code/Makefile
])

## ‘AC_OUTPUT’ line is a closing command that actually produces the part of the script in charge of creating the files registered with ‘AC_CONFIG_HEADERS’ and ‘AC_CONFIG_FILES’
AC_OUTPUT