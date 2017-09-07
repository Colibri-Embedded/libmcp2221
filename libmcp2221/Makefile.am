ACLOCAL_AMFLAGS = -I m4

pkgconfigdir=$(libdir)/pkgconfig
pkgconfig_DATA=pc/libmcp2221.pc

AM_CPPFLAGS = $(CFLAGS_LIBUSB) $(CFLAGS_LIBHIDAPI)

lib_LTLIBRARIES = libmcp2221.la
libmcp2221_la_SOURCES = libmcp2221.c
libmcp2221_la_LDFLAGS = $(LTLDFLAGS) $(PTHREAD_CFLAGS)
libmcp2221_la_LIBADD = $(LIBS_LIBUSB) $(LIBS_LIBHIDAPI)

hdrdir = $(includedir)/libmcp2221
hdr_HEADERS = $(top_srcdir)/libmcp2221.h

SCMCLEAN_TARGETS= \
 aclocal.m4 \
 config.guess \
 config.sub \
 configure \
 config.h.in \
 depcomp \
 install-sh \
 ltmain.sh \
 missing \
 mac/Makefile.in \
 testgui/Makefile.in \
 libusb/Makefile.in \
 Makefile.in \
 linux/Makefile.in \
 windows/Makefile.in \
 m4/libtool.m4 \
 m4/lt~obsolete.m4 \
 m4/ltoptions.m4 \
 m4/ltsugar.m4 \
 m4/ltversion.m4 \
 *~ \
 compile \
 ar-lib

SCMCLEAN_DIR_TARGETS = \
 autom4te.cache

scm-clean: distclean
	rm -f $(SCMCLEAN_TARGETS)
	rm -Rf $(SCMCLEAN_DIR_TARGETS)
