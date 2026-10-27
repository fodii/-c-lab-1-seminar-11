CC ?= gcc
CFLAGS ?= -O2 -Wall -Wextra -std=c11

.PHONY: all clean

all: loadgen

loadgen: main.c stats.c stats.h ../../build/lib/libcommon.a
	$(CC) $(CFLAGS) -I../../include main.c stats.c ../../build/lib/libcommon.a -o loadgen

clean:
	rm -f loadgen

