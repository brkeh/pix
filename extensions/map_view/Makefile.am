if ENABLE_LIBCHAMPLAIN

extensiondir = $(pkglibdir)/extensions
extension_LTLIBRARIES = libmap_view.la

libmap_view_la_SOURCES = 	\
	gth-map-view.c		\
	gth-map-view.h		\
	main.c

libmap_view_la_CPPFLAGS = $(PIX_CFLAGS) $(LIBCHAMPLAIN_CFLAGS) -I$(top_srcdir) -I$(top_builddir)/pix 
libmap_view_la_LDFLAGS = $(EXTENSION_LIBTOOL_FLAGS)
libmap_view_la_LIBADD = $(PIX_LIBS) $(LIBCHAMPLAIN_LIBS)
libmap_view_la_DEPENDENCIES = $(top_builddir)/pix/pix$(EXEEXT)

extensioninidir = $(extensiondir)
extensionini_DATA = $(extensionini_in_files:.extension.in.in=.extension)
DISTCLEANFILES = $(extensionini_DATA)

endif

extensionini_in_files = map_view.extension.in.in

@PIX_EXTENSION_IN_RULE@
@PIX_EXTENSION_RULE@

EXTRA_DIST = $(extensionini_in_files)

-include $(top_srcdir)/git.mk
