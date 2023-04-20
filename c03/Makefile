hello1: hello2 # now "hello2" is the pre-requisite, hence it is run first anytime "hello1" needs to run
	touch hello1
# assuming that there is no files by name "hello1" and "hello2" already exist,
# "hello2" and then "hello1" is run when "make" or "make hello1" is executed
# but when "make hello2" is executed, only "hello2" is run not "hello1"
hello2:
	touch hello2