# Copyright 2021 David Anderson
# This Makefile.am is hereby placed in the public domain
### Any error in thie file will lead to:
### error: Something went wrong bootstrapping makefile fragments
### for automatic dependency tracking
###Entering directory '/var/tmp/bld/src/lib/libdwarf'
###CC       libdwarf_la-dwarf_abbrev.lo
###/bin/bash: ../../../libtool: No such file or directory
### with no hint as to what the problem really is..

AUTOMAKE_OPTIONS = subdir-objects

MAINTAINERCLEANFILES = Makefile.in

CLEANFILES =
EXTRA_DIS  =

TESTS =  test_dwarfstring test_extra_flag_strings \
  test_linkedtopath test_headersok test_dwgetopt \
  test_makenametest test_helpertree test_macrocheck \
  test_testesb   test_sectionbitmaps

check_PROGRAMS = test_dwarfstring test_extra_flag_strings \
  test_linkedtopath test_headersok test_dwgetopt \
 test_makenametest test_helpertree test_macrocheck \
 test_testesb   test_sectionbitmaps


test_dwarfstring_SOURCES = test_dwarfstring.c \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.h \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.c
test_dwarfstring_CFLAGS = $(CFLAGS_WARN)
test_dwarfstring_CPPFLAGS = \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/lib/libdwarf

test_extra_flag_strings_SOURCES = test_extra_flag_strings.c \
   $(top_srcdir)/src/lib/libdwarf/pro_log_extra_flag_strings.c \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.h \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.c
test_extra_flag_strings_CFLAGS = $(CFLAGS_WARN)
test_extra_flag_strings_CPPFLAGS =  -DTESTING \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/lib/libdwarf

test_linkedtopath_SOURCES = test_linkedtopath.c \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.h \
   $(top_srcdir)/src/lib/libdwarf/dwarfstring.c \
   $(top_srcdir)/src/lib/libdwarf/dwarf_debuglink.h \
   $(top_srcdir)/src/lib/libdwarf/dwarf_debuglink.c \
   $(top_srcdir)/src/lib/libdwarf/dwarf_error.h
test_linkedtopath_CFLAGS = $(RO_CFLAGS_WARN) -DTESTING
test_linkedtopath_CPPFLAGS = -DTESTING \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/lib/libdwarf

# Just ensures the headers usable, no C source errors.
test_headersok_SOURCES = test_headersok.c \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_386.h  \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_mips.h  \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_ppc.h   \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_arm.h    \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_ppc64.h  \
    $(top_srcdir)/src/lib/libdwarf/dwarf_reloc_x86_64.h
test_headersok_CFLAGS = $(RO_CFLAGS_WARN)
test_headersok_CPPFLAGS = -DTESTING \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/lib/libdwarf

test_dwgetopt_SOURCES = getopttest.c \
    $(top_srcdir)/src/bin/dwarfdump/dwgetopt.h \
    $(top_srcdir)/src/bin/dwarfdump/dwgetopt.c
test_dwgetopt_CFLAGS = $(RO_CFLAGS_WARN)
test_dwgetopt_CPPFLAGS =  -DTESTING \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/bin/dwarfdump

test_makenametest_SOURCES = makename_test.c \
    $(top_srcdir)/src/bin/dwarfdump/esb.c \
    $(top_srcdir)/src/bin/dwarfdump/makename.c \
    $(top_srcdir)/src/bin/dwarfdump/dwarf_tsearchbal.c
test_makenametest_CFLAGS = $(RO_CFLAGS_WARN)
test_makenametest_CPPFLAGS =  -DTESTING \
-I$(top_srcdir) -I$(top_builddir) \
-I$(top_srcdir)/src/bin/dwarfdump \
-I$(top_srcdir)/src/lib/libdwarf

test_helpertree_SOURCES = helpertree_test.c \
    $(top_srcdir)/src/bin/dwarfdump/helpertree.c \
    $(top_srcdir)/src/bin/dwarfdump/dwarf_tsearchbal.c 
test_helpertree_FLAGS = $(RO_CFLAGS_WARN)
test_helpertree_CPPFLAGS =  -DTESTING \
-I$(top_srcdir) -I$(top_builddir) \
-I$(top_srcdir)/src/bin/dwarfdump \
-I$(top_srcdir)/src/lib/libdwarf

test_macrocheck_SOURCES = \
    $(top_srcdir)/src/bin/dwarfdump/macrocheck.c \
    $(top_srcdir)/src/bin/dwarfdump/esb.c \
    $(top_srcdir)/src/bin/dwarfdump/dwarf_tsearchbal.c 
test_macrocheck_FLAGS = $(RO_CFLAGS_WARN)
test_macrocheck_CPPFLAGS =  -DSELFTEST \
-I$(top_srcdir) -I$(top_builddir) \
-I$(top_srcdir)/src/bin/dwarfdump \
-I$(top_srcdir)/src/lib/libdwarf

test_testesb_SOURCES = testesb.c \
    $(top_srcdir)/src/bin/dwarfdump/esb.c \
    $(top_srcdir)/src/bin/dwarfdump/dwarf_tsearchbal.c 
test_testesb_FLAGS = $(RO_CFLAGS_WARN)
test_testesb_CPPFLAGS = -DTESTING \
-I$(top_srcdir) -I$(top_builddir) -I$(top_srcdir)/src/bin/dwarfdump

test_sectionbitmaps_SOURCES = section_bitmaps_test.c \
    $(top_srcdir)/src/bin/dwarfdump/section_bitmaps.c
test_sectionbitmaps_FLAGS = $(RO_CFLAGS_WARN)
test_sectionbitmaps_CPPFLAGS =  -DTESTING \
-I$(top_srcdir) -I$(top_builddir) \
-I$(top_srcdir)/src/bin/dwarfdump \
-I$(top_srcdir)/src/lib/libdwarf

TESTS += runtestdd.sh

if HAVE_DWARFEXAMPLE
TESTS += runtestsexample.sh
endif

###if HAVE_DWARFGEN
###SUBDIRS += src/bin/dwarfgen
###endif

AM_TESTS_ENVIRONMENT = DWTOPSRCDIR='$(top_srcdir)'; export DWTOPSRCDIR ; DWCOMPILERFLAGS='$(DWARF_CFLAGS_WARN)'; export DWCOMPILERFLAGS ;


EXTRA_DIST= \
buildingdummy.sh \
debuglink2.base \
debuglink.base \
dummyexecutable \
dummyexecutable.c \
dummyexecutable.debug \
dwarf_leb_test.c \
dwarf_tied_test.c \
getopttest.c \
helpertree_test.c \
makename_test.c \
runtestdd.sh \
runtestsexample.sh \
runtests.sh \
section_bitmaps_test.c \
testdebuglink.sh \
test_dwarfstring.c \
testesb.c \
test_extra_flag_strings.c \
test_headersok.c \
test_linkedtopath.c \
test-mach-o-32.base \
test-mach-o-32.dSYM \
testobjLE32PE.base \
testobjLE32PE.exe \
testobjLE32PE.test.c \
testuriLE64ELf.base \
testuriLE64ELf.obj 
