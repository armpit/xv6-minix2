TOP_SRCDIR = ../..
include $(TOP_SRCDIR)/Makefile.common

INCLDIR=$(TOP_SRCDIR)/include
# I've removed -Wall from the CFLAGS:	Warren
CFLAGS = -fno-builtin -m32 -Werror -nostdinc -I$(INCLDIR) -D_POSIX_SOURCE
CFLAGS += $(shell $(CC) -fno-stack-protector -E -x c /dev/null >/dev/null 2>&1 && echo -fno-stack-protector)

all: regcomp.o regerror.o regexec.o regfree.o

clean:
	rm -f *.o
