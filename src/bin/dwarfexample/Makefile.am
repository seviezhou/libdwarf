###Copyright (C) 2018 Vincent Torri <vincent dot torri at gmail dot com
###This code is public domain and can be freely used or copied.

MAINTAINERCLEANFILES = Makefile.in

AUTOMAKE_OPTIONS = subdir-objects

bin_PROGRAMS = simplereader frame1 findfuncbypc dwdebuglink
dwarfbigend=@DWARF_BIGENDIAN@

simplereader_SOURCES = simplereader.c
simplereader_CPPFLAGS = -I$(top_srcdir)/src/lib/libdwarf \
  -I$(top_builddir)/src/lib/libdwarf
simplereader_CFLAGS = $(DWARF_CFLAGS_WARN)
simplereader_LDADD = $(top_builddir)/src/lib/libdwarf/libdwarf.la \
$(DWARF_LIBS)

frame1_SOURCES = frame1.c
frame1_CPPFLAGS = -I$(top_srcdir)/src/lib/libdwarf \
  -I$(top_builddir)/src/lib/libdwarf
frame1_CFLAGS = $(DWARF_CFLAGS_WARN)
frame1_LDADD = $(top_builddir)/src/lib/libdwarf/libdwarf.la \
$(DWARF_LIBS)

findfuncbypc_SOURCES = findfuncbypc.c
findfuncbypc_CPPFLAGS = -I$(top_srcdir)/src/lib/libdwarf \
  -I$(top_builddir)/src/lib/libdwarf
findfuncbypc_CFLAGS = $(DWARF_CFLAGS_WARN)
findfuncbypc_LDADD = $(top_builddir)/src/lib/libdwarf/libdwarf.la \
$(DWARF_LIBS)

dwdebuglink_SOURCES = dwdebuglink.c
dwdebuglink_CPPFLAGS = -I$(top_srcdir)/src/lib/libdwarf \
  -I$(top_builddir)/libdwarf
dwdebuglink_CFLAGS = $(DWARF_CFLAGS_WARN)
dwdebuglink_LDADD = $(top_builddir)/src/lib/libdwarf/libdwarf.la \
$(DWARF_LIBS)

EXTRA_DIST = \
ChangeLog \
ChangeLog2009 \
ChangeLog2010 \
ChangeLog2011 \
ChangeLog2012 \
ChangeLog2013 \
ChangeLog2014 \
ChangeLog2015 \
ChangeLog2016 \
ChangeLog2017 \
ChangeLog2018 \
CMakeLists.txt \
simplecrc.c \
NEWS \
$(dwarfexample_DATA)
