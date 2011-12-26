CFLAGS = -g
CFLAGS_LIB = -g -c

CC = gcc
LD = ld
AR = ar

all:  wikix 

libcutf8.a: utf8.o
	$(AR) r libcutf8.a utf8.o

wikix: wikix.c libcutf8.a 
	$(CC) $(CFLAGS) wikix.c -o wikix libcutf8.a -lssl -lcrypto

clean:
	rm -f *.o *.a wikix     

install: all
	install -m 755 wikix /usr/sbin