CC ?= gcc
CFLAGS ?= -O2 -Wall -Wextra -std=c11

.PHONY: all clean

all: backend

backend: main.c handler.c handler.h ../../build/lib/libcommon.a
	$(CC) $(CFLAGS) -I../../include main.c handler.c ../../build/lib/libcommon.a -o backend

clean:
	rm -f backend

