all: 
	gcc -c -Wall -Werror -fpic serial_cmd.c
	gcc -shared -o libserial_cmd.so serial_cmd.o
	cp ./libserial_cmd.so /usr/lib
	chmod 0755 /usr/lib/libserial_cmd.so
	ldconfig
	gcc -Wall -o sendcmd sendcmd.c -lserial_cmd
