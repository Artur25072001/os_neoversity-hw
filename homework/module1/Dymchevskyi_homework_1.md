<!-- 2 СHAPTER -->

vboxuser@Test:~$ man ls -->
vboxuser@Test:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
Change the shell working directory.

    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.

    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.

    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.

    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes

    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.

    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.

vboxuser@Test:~$ man cat
vboxuser@Test:~$ man man
man: can't resolve man7/groff_man.7
vboxuser@Test:~$
vboxuser@Test:~$ cp --help
Usage: cp [OPTION]... [-T] SOURCE DEST
or: cp [OPTION]... SOURCE... DIRECTORY
or: cp [OPTION]... -t DIRECTORY SOURCE...
Copy SOURCE to DEST, or multiple SOURCE(s) to DIRECTORY.

Mandatory arguments to long options are mandatory for short options too.
-a, --archive same as -dR --preserve=all
--attributes-only don't copy the file data, just the attributes
--backup[=CONTROL] make a backup of each existing destination file
-b like --backup but does not accept an argument
--copy-contents copy contents of special files when recursive
-d same as --no-dereference --preserve=links
--debug explain how a file is copied. Implies -v
-f, --force if an existing destination file cannot be
opened, remove it and try again (this option
is ignored when the -n option is also used)
-i, --interactive prompt before overwrite (overrides a previous -n
option)
-H follow command-line symbolic links in SOURCE
-l, --link hard link files instead of copying
-L, --dereference always follow symbolic links in SOURCE
-n, --no-clobber do not overwrite an existing file and do not fail
(overrides a -u or previous -i option). See also
--update; equivalent to --update=none.
-P, --no-dereference never follow symbolic links in SOURCE
-p same as --preserve=mode,ownership,timestamps
--preserve[=ATTR_LIST] preserve the specified attributes
--no-preserve=ATTR_LIST don't preserve the specified attributes
--parents use full source file name under DIRECTORY
-R, -r, --recursive copy directories recursively
--reflink[=WHEN] control clone/CoW copies. See below
--remove-destination remove each existing destination file before
attempting to open it (contrast with --force)
--sparse=WHEN control creation of sparse files. See below
--strip-trailing-slashes remove any trailing slashes from each SOURCE
argument
-s, --symbolic-link make symbolic links instead of copying
-S, --suffix=SUFFIX override the usual backup suffix
-t, --target-directory=DIRECTORY copy all SOURCE arguments into DIRECTORY
-T, --no-target-directory treat DEST as a normal file
--update[=UPDATE] control which existing files are updated;
UPDATE={all,none,older(default)}. See below
-u equivalent to --update[=older]
-v, --verbose explain what is being done
-x, --one-file-system stay on this file system
-Z set SELinux security context of destination
file to default type
--context[=CTX] like -Z, or if CTX is specified then set the
SELinux or SMACK security context to CTX
--help display this help and exit
--version output version information and exit

ATTR_LIST is a comma-separated list of attributes. Attributes are 'mode' for
permissions (including any ACL and xattr permissions), 'ownership' for user
and group, 'timestamps' for file timestamps, 'links' for hard links, 'context'
for security context, 'xattr' for extended attributes, and 'all' for all
attributes.

By default, sparse SOURCE files are detected by a crude heuristic and the
corresponding DEST file is made sparse as well. That is the behavior
selected by --sparse=auto. Specify --sparse=always to create a sparse DEST
file whenever the SOURCE file contains a long enough sequence of zero bytes.
Use --sparse=never to inhibit creation of sparse files.

UPDATE controls which existing files in the destination are replaced.
'all' is the default operation when an --update option is not specified,
and results in all existing files in the destination being replaced.
'none' is similar to the --no-clobber option, in that no files in the
destination are replaced, but also skipped files do not induce a failure.
'older' is the default operation when --update is specified, and results
in files being replaced if they're older than the corresponding source file.

When --reflink[=always] is specified, perform a lightweight copy, where the
data blocks are copied only when modified. If this is not possible the copy
fails, or if --reflink=auto is specified, fall back to a standard copy.
Use --reflink=never to ensure a standard copy is performed.

The backup suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.
The version control method may be selected via the --backup option or through
the VERSION_CONTROL environment variable. Here are the values:

none, off never make backups (even if --backup is given)
numbered, t make numbered backups
existing, nil numbered if numbered backups exist, simple otherwise
simple, never always make simple backups

As a special case, cp makes a backup of SOURCE when the force and backup
options are given and SOURCE and DEST are the same name for an existing,
regular file.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/cp>
or available locally via: info '(coreutils) cp invocation'
vboxuser@Test:~$ mv --help
Usage: mv [OPTION]... [-T] SOURCE DEST
or: mv [OPTION]... SOURCE... DIRECTORY
or: mv [OPTION]... -t DIRECTORY SOURCE...
Rename SOURCE to DEST, or move SOURCE(s) to DIRECTORY.

Mandatory arguments to long options are mandatory for short options too.
--backup[=CONTROL] make a backup of each existing destination file
-b like --backup but does not accept an argument
--debug explain how a file is copied. Implies -v
-f, --force do not prompt before overwriting
-i, --interactive prompt before overwrite
-n, --no-clobber do not overwrite an existing file
If you specify more than one of -i, -f, -n, only the final one takes effect.
--no-copy do not copy if renaming fails
--strip-trailing-slashes remove any trailing slashes from each SOURCE
argument
-S, --suffix=SUFFIX override the usual backup suffix
-t, --target-directory=DIRECTORY move all SOURCE arguments into DIRECTORY
-T, --no-target-directory treat DEST as a normal file
--update[=UPDATE] control which existing files are updated;
UPDATE={all,none,older(default)}. See below
-u equivalent to --update[=older]
-v, --verbose explain what is being done
-Z, --context set SELinux security context of destination
file to default type
--help display this help and exit
--version output version information and exit

UPDATE controls which existing files in the destination are replaced.
'all' is the default operation when an --update option is not specified,
and results in all existing files in the destination being replaced.
'none' is similar to the --no-clobber option, in that no files in the
destination are replaced, but also skipped files do not induce a failure.
'older' is the default operation when --update is specified, and results
in files being replaced if they're older than the corresponding source file.

The backup suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.
The version control method may be selected via the --backup option or through
the VERSION_CONTROL environment variable. Here are the values:

none, off never make backups (even if --backup is given)
numbered, t make numbered backups
existing, nil numbered if numbered backups exist, simple otherwise
simple, never always make simple backups

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/mv>
or available locally via: info '(coreutils) mv invocation'
vboxuser@Test:~$

Відповіді на питання

1.Ключ ls, що показує приховані файли: -a (або --all).

2.Ключ cat, що нумерує рядки: -n.

3.Чим відрізняються man та --help:

man (manual): Виводить детальну, повну інструкцію до команди, включаючи опис усіх прапорців, параметрів та прикладів використання. Грубо кажучи суха документація,бібліотека

--help: Виводить стислу довідку про синтаксис та основні ключі команди прямо в терміналі. Коротка довідка

<!-- 3 CHAPTER -->

vboxuser@Test:~$ cd /tmp
vboxuser@Test:/tmp$ mkdir test_dir
vboxuser@Test:/tmp$ cd test_dir
vboxuser@Test:/tmp/test_dir$ > my_file.txt
vboxuser@Test:/tmp/test_dir$ ls -l
total 0
-rw-rw-r-- 1 vboxuser vboxuser 0 Mar 8 17:59 my_file.txt
vboxuser@Test:/tmp/test_dir$ cat my_file.txt
vboxuser@Test:/tmp/test_dir$ cat --help
Usage: cat [OPTION]... [FILE]...
Concatenate FILE(s) to standard output.

With no FILE, or when FILE is -, read standard input.

-A, --show-all equivalent to -vET
-b, --number-nonblank number nonempty output lines, overrides -n
-e equivalent to -vE
-E, --show-ends display $ at end of each line
-n, --number number all output lines
-s, --squeeze-blank suppress repeated empty output lines
-t equivalent to -vT
-T, --show-tabs display TAB characters as ^I
-u (ignored)
-v, --show-nonprinting use ^ and M- notation, except for LFD and TAB
--help display this help and exit
--version output version information and exit

Examples:
cat f - g Output f's contents, then standard input, then g's contents.
cat Copy standard input to standard output.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/cat>
or available locally via: info '(coreutils) cat invocation'
vboxuser@Test:/tmp/test_dir$
