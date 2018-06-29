build:
	make clean
	gcc -c add.c
	gcc -c sub.c
	ar rs libheymath.a add.o sub.o
	gcc -I . -c main.c
	gcc -o exec_main main.o libheymath.a

run:
	./exec_main

clean:
	rm -rf *.o *.a exec_main
