CC ?= gcc
CFLAGS ?= -O2 -Wall -Wextra -std=c11

.PHONY: all clean

all: balancer

balancer: main.c router.c router.h ../../build/lib/libcommon.a
	$(CC) $(CFLAGS) -I../../include main.c router.c ../../build/lib/libcommon.a -o balancer

clean:
	rm -f balancer

