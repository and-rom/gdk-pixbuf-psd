AUTOMAKE_OPTIONS = foreign
ACLOCAL_AMFLAGS = -I m4 ${ACLOCAL_FLAGS}

loaderdir = $(GDK_PIXBUF_DIR)
loader_LTLIBRARIES = libpixbufloader-psd.la

INCLUDES = $(GDKPIXBUF_CFLAGS) $(GLIB_CFLAGS) $(GMODULE_CLAGS)

libpixbufloader_psd_la_SOURCES = io-psd.c
libpixbufloader_psd_la_LDFLAGS = -export_dynamic -avoid-version -module -no-undefined $(AM_CPPFLAGS)
libpixbufloader_psd_la_LIBADD = $(GDKPIXBUF_LIBS) $(GLIB_LIBS) $(GMODULE_LIBS)

