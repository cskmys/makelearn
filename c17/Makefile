objects = foo.o bar.o all.o
all: ${objects}
# implicitly means link all the 3 ".o" files to generate "all"
${objects}: %.o: %.c
# equivalent to writing:
# foo.o: foo.c
# bar.o: bar.c
# all.o: all.c
# using implicit rules

all.c:
	echo "int main(){ return 0; }" > all.c

%.c:
	touch ${@}
# since "all.c" already has a target the remaining: "foo.c", "bar.c" will come here

clean:
	rm -f *.c *.o all
