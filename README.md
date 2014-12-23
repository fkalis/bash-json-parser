bash-json-parser
================

A little bash script that converts a JSON string into key value pairs. This script has no dependencies to other tools like `grep` or `sed`, it relies purely on bash commands.

If you want better performance or more configuration options, I suggest using other solutions like [jq](https://github.com/stedolan/jq) or [JSON.sh](https://github.com/dominictarr/JSON.sh). Both projects can be found here at Github.

Usage
-----

You can either use a pipe or parameters to convert your JSON string into a list of key-value-pairs.

	cat example.json | ./bash-json-parser
	./bash-json-parser '{ "a": "b", "c": [ "hallo", "welt" ] }'

The latter will produce the following output

	a=b
    c.0=hallo
    c.1=welt

Hints
-----

This script does not validate your input, so if your input has an incorrect syntax, I can not promise, that the output is in any way usable.
