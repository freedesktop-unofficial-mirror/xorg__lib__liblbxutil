dnl 
dnl  $Id$
dnl 
dnl  Copyright © 2003 Keith Packard, Noah Levitt
dnl 
dnl  Permission to use, copy, modify, distribute, and sell this software and its
dnl  documentation for any purpose is hereby granted without fee, provided that
dnl  the above copyright notice appear in all copies and that both that
dnl  copyright notice and this permission notice appear in supporting
dnl  documentation, and that the name of Keith Packard not be used in
dnl  advertising or publicity pertaining to distribution of the software without
dnl  specific, written prior permission.  Keith Packard makes no
dnl  representations about the suitability of this software for any purpose.  It
dnl  is provided "as is" without express or implied warranty.
dnl 
dnl  KEITH PACKARD DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
dnl  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
dnl  EVENT SHALL KEITH PACKARD BE LIABLE FOR ANY SPECIAL, INDIRECT OR
dnl  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
dnl  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
dnl  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
dnl  PERFORMANCE OF THIS SOFTWARE.
dnl
dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])

dnl
dnl Version should match the current XFixes version. XFixesQueryVersion
dnl returns the version from xfixeswire.h, NOT the version we set here. But we
dnl try to keep these the same.  Note that the library has an extra
dnl digit in the version number to track changes which don't affect the
dnl protocol, so Xfixes version l.n.m corresponds to protocol version l.n,
dnl that 'revision' number appears in Xfixes.h and has to be manually
dnl synchronized.
dnl
AC_INIT(lbxutil, 1.0.0, [sandmann@redhat.com], liblbxutil)
AM_INIT_AUTOMAKE([dist-bzip2])
AM_MAINTAINER_MODE

AM_CONFIG_HEADER(config.h)

# Check for progs
AC_PROG_CC
AC_PROG_LIBTOOL

# Check for X
PKG_CHECK_MODULES(DEP, xextproto)

AC_SUBST(DEP_CFLAGS)
AC_SUBST(DEP_LIBS)
		  
# Check fixesext configuration, strip extra digits from package version to
# find the required protocol version

AC_OUTPUT([Makefile
	   src/Makefile
	   lbxutil.pc])