test: test.o # multi-step compilation: generating executable from linking object
	gcc test.o -o test

test.o: test.c # multi-step compilation: generating object from source
	gcc -c test.c -o test.o

test.c: # will be run only if you delete "test.c", it won't run if you edit it
	echo "int main(){ return 0; }" > test.c

# if you do "make" all 3 targets will be run
# if you delete:
# "test" file, then only "test" target will be run
# "test.o" file, then "test.o" target will be run, the new "test.o" file will be newer than "test" file, hence, "test" target will be run
# "test.c" file, then "test.c" target is not up to date, which will cause "test.o" target to not be up to date, which will cause "test" target to not be up to date. Hence, all the 3 will be run.