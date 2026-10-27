CC ?= gcc
CFLAGS ?= -O2 -Wall -Wextra -std=c11

.PHONY: all clean

all: ../build/lib/libcommon.a

../build/lib/libcommon.a: net.c http.c utils.c ../include/net.h ../include/http.h ../include/utils.h
	mkdir -p ../build/lib
	$(CC) $(CFLAGS) -I../include -c net.c http.c utils.c
	ar rcs ../build/lib/libcommon.a net.o http.o utils.o

clean:
	rm -f net.o http.o utils.o ../build/lib/libcommon.a
