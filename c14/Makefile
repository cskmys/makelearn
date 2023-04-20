var = *.o # no files matching the wildcard, so "var" takes "*.o" literally 
var_wrap = $(wildcard *.o) # no files matching the wildcard, but its wrapped in "wildcard" function, so "var_wrap" is empty

print: # "make" will run this target
	echo ${var}
	echo ${var_wrap}

print_var: ${var} # "make print_var" has dependency "var" which is "*.o", as there are no targets here by name "*.o", it throws an error
	echo ${var}

print_var_wrap: ${var_wrap} # "make print_var_wrap" finds that dependency "var_wrap" is empty, and hence runs target "print_var_wrap"
	echo ${var_wrap}