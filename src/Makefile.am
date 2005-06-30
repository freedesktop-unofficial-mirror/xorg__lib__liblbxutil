lib_LTLIBRARIES = liblbxutil.la

noinst_PROGRAMS = mkg3states

mkg3states_SOURCES =				\
	$(srcdir)/image/mkg3states.c

BUILT_SOURCES =					\
	g3states.h

liblbxutil_la_SOURCES =				\
	$(srcdir)/lbx_zlib/reqstats.h		\
	$(srcdir)/lbx_zlib/lbx_zlib_io.c	\
	$(srcdir)/lbx_zlib/lbx_zlib.h		\
	$(srcdir)/lbx_zlib/lbx_zlib.c		\
	$(srcdir)/lbx_zlib/reqstats.c		\
	$(srcdir)/image/misc.c			\
	$(srcdir)/image/dpackbits.c		\
	$(srcdir)/image/epackbits.c		\
	$(srcdir)/image/dfaxg42d.c		\
	g3states.h				\
	$(srcdir)/image/lbxfax.h		\
	$(srcdir)/image/efaxg42d.c		\
	$(srcdir)/image/lbxbwcodes.h		\
	$(srcdir)/delta/lbxdelta.c

liblbxutil_la_LIBADD = @DEP_LIBS@

INCLUDES = @DEP_CFLAGS@ 

g3states.h: mkg3states
	./mkg3states > g3states.h_ && mv g3states.h_ g3states.h

#
# Library version info.  Check the libtool docs for
# instructions on when and how to change this value
#
# bump when the ABI changes
LBXUTIL_CURRENT=2
# bump for non-ABI changes, reset to zero when CURRENT changes
LBXUTIL_REVISION=0
# bump when the ABI changes in backward-compatible fashion
LBXUTIL_AGE=2
liblbxutil_la_LDFLAGS = -version-info ${LBXUTIL_CURRENT}:${LBXUTIL_REVISION}:${LBXUTIL_AGE}

CLEANFILES = g3states.h
