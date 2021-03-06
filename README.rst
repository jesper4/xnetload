=============================
X11 network monitor for Linux
=============================

Purpose
-------
This program displays network traffic and uptime for the network connection
named on the command line. It was originally written it to monitor dial-up
connections. It requires the ``/proc`` file system.

New versions
------------
New versions of this program are always on github:
https://github.com/rsmith-nl/xnetload

Files
-----
The distribution should contain the following files:
COPYING         GNU General Public License.
Makefile        Makefile for GNU make.
Makefile.static Makefile for a statically linked executable.
README.rst      :-)
ChangeLog       Changes between different versions.
XNetload        Application defaults file for xnetload.
xnetload.1      Manual page.
depend          Dependency information for the compiler.
data.c          Data-collecting code.
data.h          Header for data collecting code.
x11-ui.c        Xt/Xaw user interface code.

Building and installing the program
-----------------------------------

* If you want a statically linked binary, copy Makefile.static to Makefile.
* To build the program invoke 'make'. The default is to build a optimized
  binary. You can uncomment the first set of CFLAGS and LFLAGS (and comment
  out the second set) for a debugging binary.
* To install the program, invoke ``make install`` *as root*.
* Optionally, edit the application-defaults file (``XNetload``), and copy it
  (as root) to a place where X can find it. Usually a ``app-defaults``
  directory in the X directory tree. On my system it is the
  ``/var/X11R6/lib/app-defaults`` directory.

If you don't like it, login as root, change to the source directory and run
'make uninstall'. After that you can remove the source tree.

Contacting the author
---------------------
For questions, remarks and bug reports about the source release contact
the author at the following addresses.

    e-mail: rsmith@xs4all.nl

The author only release source code packages. This is the best way to work
around library versions and related difficulties. (It also means that other
people, using the source, can find bugs :-) If you want to build a binary
package, by all means do so, but please identify it as your doing and
responsibility.
