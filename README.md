# symlinks

Scan/change symbolic links.

Symlinks is a simple tool that helps find and remedy problematic symbolic links on a system.


## Description

Symlinks scans directories for symbolic links, identifying dangling, relative, absolute, messy, and other_fs links.  It can also change absolute links to relative within a given filesystem.


# To install

```sh
make clobber all
sudo make install clobber
```


# To use

```sh
/usr/local/bin/symlinks [-cdorstvV] dirlist ..

    -c  change absolute/messy links to relative
	-d  delete dangling links
	-o  warn about links across file systems
	-r  recurse into subdirs
	-s  shorten lengthy links (displayed in output only when -c not specified)
	-t  show what would be done by -c
	-v  verbose (show all symlinks)
	-V  print version string and exit

symlinks: scan/change symbolic links - 1.4.4 2025-04-06
```


### Scan:

    $ symlinks -r [path]


### Show all symlinks:

    $ symlinks -rv [path]


### Convert absolute symlink to relative:

    $ symlinks -rc [path]


### More options:

    $ symlinks -h


## Changes

#### v1.4.4 2025-04-06
- Minor code mods and GitHub packaging mods.
- Updated man page.

#### v1.4.3
- Fixed LFS support bug that caused erratic behavior on 32-bit systems.

#### v1.4.2
- Reformatted for readability roughly based on Google style guide.
- Fixed loss of precision due to implicit type conversion.
- Minor documentation updates.

#### v1.4-1
- Added Mac OS X compatibility.

#### v1.4
- Incorporate patches from Fedora.

#### v1.3
- More messy-link fixes, new `-o` flag for other_fs.

#### v1.2
- Added `-s` flag to shorten links with redundant path elements.
- Also includes code to remove excess slashes from paths.


## Credit

Symlinks was created by **Mark Lord** <mlord@pobox.com>.
Maintained by **J. Brandt Buckley** <brandt@runlevel1.com>.

Additional modifications by: chongo (Landon Curt Noll) [https://github.com/lcn2](https://github.com/lcn2).

See: [https://github.com/lcn2/symlinks](https://github.com/lcn2/symlinks)

Share and enjoy!  :-)


# Reporting Security Issues

To report a security issue, please visit "[Reporting Security Issues](https://github.com/lcn2/symlinks/security/policy)".
