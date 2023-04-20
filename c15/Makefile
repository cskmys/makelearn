CC = gcc
CFLAGS = -g # debug info flag to be used via implicitly running the compilation command

test: test.o # implicitly "test" is built via "test.o", and "test.o" is built via "test.c"

test.c:
	echo "int main(){ return 0; }" > test.c

clean:
	rm -f test*