TOP=$(abspath ../../..)
include $(TOP)/defs.mak
SUBBINDIR=$(BINDIR)

PROGRAM = jsonprint

SOURCES = $(wildcard *.c)

INCLUDES = -I$(INCDIR)

CFLAGS = $(OEHOST_CFLAGS) $(GCOV_CFLAGS)

LDFLAGS = $(OEHOST_LDFLAGS) $(GCOV_LDFLAGS)

LIBS += $(LIBDIR)/libmysthost.a
LIBS += $(LIBDIR)/libjson.a
LIBS += $(LIBDIR)/libmystutils.a

REDEFINE_TESTS=1

include $(TOP)/rules.mak

tests:
	$(PREFIX) $(SUBBINDIR)/jsonprint sample.json > /dev/null
