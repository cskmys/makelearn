all:
	cd ..; echo ${PWD} # "PWD" is a shell variable which will get replaced with the directory where "make" command was executed even before executing "cd .." hence, you'll not get the impact of "cd .."

	cd ..; echo $$PWD # If you escape "$" with "$" then when the "make" command is executed, you'll get "cd ..; echo $PWD" instead of "cd ..; echo <path>" like above, now "cd .." will have an impact over it

	cd ..; pwd # "pwd" is a command which will output the working directory at the time of its execution, hence, "cd .." has an impact over it

	cd ..; echo `pwd` # "echo `pwd`" will execute "pwd" and output its result, nothing is replaced or executed before running "cd ..". hence "cd .." has an impact over it
