files = one two three # variables can be assigned using "=" or ":="
all: ${files} # variables can be referenced using "${}" or "$()"

${files}:
	touch $@

clean:
	rm -f ${files}