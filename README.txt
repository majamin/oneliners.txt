README.txt
----------

This is a collection of oneliners, commands, scripts, etc. for UNIX-like systems.
PRs are welcome - oneliners need to be in the format (see the file):

(*) DESCRIPTION: `COMMAND`

TODO
----

* More package manager commands (dpkg, apt, yum, etc.)
* A longer TODO list

Bonus
-----

You can alias a simple command like this one:

    alias oneliner='print -z $(grep "(\*)" -rw oneliners.txt | fzf -e | sed "s/: \{1,\}/\n/" | tail -1 | sed "s/^\`//;s/\`$//")'

Which will give you a `fzf` menu and then print the command directly into the shell for editing or execution.
