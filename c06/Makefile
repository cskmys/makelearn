test: test.o # multi-step compilation: generating executable from linking object
	gcc test.o -o test

test.o: test.c # multi-step compilation: generating object from source
	gcc -c test.c -o test.o

test.c: # will be run only if you delete "test.c", it won't run if you edit it
	echo "int main(){ return 0; }" > test.c