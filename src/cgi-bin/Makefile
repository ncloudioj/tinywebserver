# Makefile of cgi-bin
#

CC = gcc
CFLAGS = -Wall -O2
INCLUDE = ../

all:adder

adder:adder.o
	$(CC) $(CFLAGS)  -o $@ $<

adder.o:adder.c
	$(CC) $(CFLAGS) -I$(INCLUDE) -c $<

.PHONY: clean
clean:
	rm -f adder adder.o	
