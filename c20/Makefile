SHELL=/bin/bash # changing the default shell used by "make" i.e. "/bin/sh"

all:
	@cd .. #@ will silence the command being printed, but not the command output
	@echo $$\{PWD\} # you can use "$" to escape "$" and "\" for "{" and "}"
	@pwd # each line of command is running independently, hence "cd .." above will not have an impact

	cd ..; \
	echo $$\{PWD\}; \
	pwd # having "\", makes all the commands into one single line and ";" combines all commands into a single compound command, hence "cd .." at the beginning can have an impact
