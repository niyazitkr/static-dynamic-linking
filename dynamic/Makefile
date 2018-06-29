#Before using the run command you should Link the dynamic library with dynamic linker
#run the following:  sudo nano /etc/ld.so.conf 
#add our directory where your dynamic library's directory
#In my case: /home/linking_example/dynamic
#run the following:  sudo ldconfig
#now your dynamic library is linked and you can run executable dy_exec

build:
	make clean
	gcc -Wall -fPIC -c add.c 
	gcc -Wall -fPIC -c sub.c
	gcc -shared -o libheymath.so add.o sub.o
	gcc -c main.c
	gcc -o dy_exec main.o libheymath.so

run:
	./dy_exec
clean:
	rm -rf *.o *.so dy_exec