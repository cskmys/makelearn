all: hello hai

hello::
	echo "hello"

hello::
	echo "hello again"
# both "hello" will be executed as there is double-colon

hai: # this won't be run as there is another one below and this has single colon
	echo "hai"

hai: # this overrides the above "hai" as there is no double-colon 
	echo "hai again"
