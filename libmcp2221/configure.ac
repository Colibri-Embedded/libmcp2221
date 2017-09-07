AC_PREREQ(2.63)

# Version number. This is currently the only place.
m4_define([LIBMCP2221_MAJOR],   1)
m4_define([LIBMCP2221_MINOR],   0)
m4_define([LIBMCP2221_RELEASE], 4)
#m4_define(LIBMCP2221_RC],        )
m4_define([VERSION_STRING], LIBMCP2221_MAJOR[.]LIBMCP2221_MINOR[.]LIBMCP2221_RELEASE)

AC_INIT([libmcp2221], [VERSION_STRING], [bug-automake@gnu.org])

AM_INIT_AUTOMAKE([-Wall -Werror foreign])

AC_PROG_CC
PKG_PROG_PKG_CONFIG

m4_ifdef([AM_PROG_AR], [AM_PROG_AR])
LT_INIT

AC_MSG_CHECKING([operating system])
AC_MSG_RESULT($host)

# Check for libusb-1.0
PKG_CHECK_MODULES([libusb], [libusb-1.0 >= 1.0.9], true)
LIBS_LIBUSB+=" $libusb_LIBS"
CFLAGS_LIBUSB+=" $libusb_CFLAGS"

# Check for hidapi-libusb
PKG_CHECK_MODULES([hidapi_libusb], [hidapi-libusb >= 0.8.0], true)
LIBS_LIBHIDAPI+=" $hidapi_libusb_LIBS"
CFLAGS_LIBHIDAPI+=" $hidapi_libusb_CFLAGS"

# Use buildin HIDAPI
#~ AM_CONDITIONAL([USE_BUILTIN_HIDAPI], [true])

AC_SUBST([LIBS_LIBHIDAPI])
AC_SUBST([LIBS_LIBUSB])
AC_SUBST([CFLAGS_LIBHIDAPI])
AC_SUBST([CFLAGS_LIBUSB])


AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([
 Makefile \
 pc/libmcp2221.pc
])
AC_OUTPUT
