.PHONY: clean

vpath print.c src
vpath hello.c src
vpath print.h incl

hello.o: hello.c
	gcc -c $<

print.o: print.c
	gcc -c $<

print.a: print.o
	ar rs $@ $<

hello: hello.o
	gcc -o $@ $^ -L./src -I./incl

hello: hello.o print.o print.a

hello.o: hello.c print.h

print.o: print.c

print.a: print.o

clean: 
	rm -f hello *.o *.a

