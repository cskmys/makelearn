obj_files = foo.res bar.o lose.o
src_files = foo.raw bar.c lose.c

all: $(obj_files)
.PHONY: all

# "filter" function outputs files that match the pattern defined by "%" wildcard
$(filter %.o,$(obj_files)): %.o: %.c # implicitly ".o" is built from ".c"

$(filter %.res,$(obj_files)): %.res: %.raw # since there are no implicit rules over ".res", it simply becomes a target to invoke ".raw" target
	echo "target: ${@} prereq: ${<}"
# if you don't add this line, then "foo.res" will be considered as an executable, and implicit rules will try to find "foo.res.o",
# which will in turn will take it to "$(filter %.o,$(obj_files)): %.o: %.c" and hence will take it to "$(wildcard %.c):" creating 
# "foo.res.c" which it will try to compile as "foo.res.o" and link "foo.res.o" as executable "foo.res"
# since "foo.res.c" is empty, so is "foo.res.o", but "foo.res" requires a "main" function and hence we get a failure. 

%.c %.raw: #pattern rule that all files with extension ".c" and ".raw" must execute the command(s) below
	touch ${@}

clean:
	rm -f $(src_files) ${obj_files}
