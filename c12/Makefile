files = one two
op_target = hey
${op_target}: ${files}
	echo ${?}
	echo ${^}
	touch ${@}

${files}:
	touch ${@}

clean:
	rm -f ${files} ${op_target}

# "${^}" always prints whatever is in variable "files"
# if you do "make", touch "one", then "make" again, you'll be able to see that "${?}" will print "one"