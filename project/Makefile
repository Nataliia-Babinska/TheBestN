.PHONY: clean
.SUFFIXES: .c .o .a
vpath %.c src
vpath %.h include

%.o: %.c
	gcc -c $<
%.o: %.h
	gcc -c $<
lib%.a: lib%.o
	ar rs $@ $<
%: %.o
	gcc -o $@ $^ -L./lib -I./incl

hello: hello.o libhello.a
hello.o: print.c print.h
libhello.a: libhello.o
libhello.o: hello.c
clean:
	rm -f hello *.o ./lib/*.a





























