AC_PREREQ(2.61)

AC_INIT(gdk-pixbuf-psd, 0.1.0, nospam@nowhere.com)
AM_INIT_AUTOMAKE([dist-bzip2 no-dist-gzip])
m4_ifdef([AM_SILENT_RULES],[AM_SILENT_RULES([yes])])

AC_CONFIG_SRCDIR([.])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])

# Checks for programs
AC_PROG_CC
AC_PROG_CXX
AM_PROG_CC_C_O
AC_PROG_LIBTOOL
PKG_PROG_PKG_CONFIG

# Checks for libraries
PKG_CHECK_MODULES(GLIB, glib-2.0)
PKG_CHECK_MODULES(GMODULE, gmodule-2.0)
PKG_CHECK_MODULES(GDKPIXBUF, gdk-pixbuf-2.0)

GDK_PIXBUF_DIR=`$PKG_CONFIG --variable=gdk_pixbuf_moduledir gdk-pixbuf-2.0`
if test -z "$GDK_PIXBUF_DIR" ; then
	GTK_VERSION=`$PKG_CONFIG --variable=gtk_binary_version gtk+-2.0`
	GDK_PIXBUF_DIR="$libdir/gtk-2.0/$GTK_VERSION/loaders"
fi
AC_SUBST(GDK_PIXBUF_DIR)

# Checks for header files0
AC_HEADER_STDC
AC_CHECK_HEADERS([stdint.h stdlib.h string.h])

AC_OUTPUT(
Makefile
)

echo "
Configuration for $PACKAGE $VERSION:
-------------------------------------------

  Install prefix .....: $prefix
  Module directory ...: $GDK_PIXBUF_DIR

  Now type 'make' to build $PACKAGE $VERSION,
  and then 'make install' for installation.
"
