CC = gcc
CFLAGS = -g

test: test.o ret.o
#now implicit rules will link "test.o" and "ret.o" to generate "test"

build_obj: test.o ret.o
.PHONY: build_obj # as its marked "PHONY" implicit rules will not create executable "build_obj" by linking "test.o" and "ret.o"

ret.c:
	echo "int get_ret(){ return 0; }" > ret.c

test.c:
	echo "extern int get_ret(); int main(){ return get_ret(); }" > test.c

clean:
	rm -f test* ret*
