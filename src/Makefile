# Makefile of tinyserver
#

CC = gcc
CFLAGS = -Wall -O2
OBJS = csapp.o
LIBS = -lpthread

all:tinyserver_prefork tinyserver_thread tinyserver_epoll adder

tinyserver_prefork:$(OBJS) tiny_prefork.o
	$(CC) $(CFLAGS) -o $@ $(OBJS) tiny_prefork.o $(LIBS)


tinyserver_thread:$(OBJS) sbuf.o tiny_thread.o
	$(CC) $(CFLAGS) -o $@ $(OBJS) sbuf.o tiny_thread.o $(LIBS)

tinyserver_epoll:$(OBJS) tiny_epoll.o
	$(CC) $(CFLAGS) -o $@ $(OBJS) tiny_epoll.o $(LIBS)

adder:
	cd cgi-bin && $(MAKE) all

%.o:%.c
	$(CC) -c $(CFLAGS) $< 

.PHONY:clean
clean:
	rm -f *.o tinyserver_prefork tinyserver_thread tinyserver_epoll
	cd cgi-bin && $(MAKE) clean
