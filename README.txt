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

You can alias a simple command like this one to get a nice menu that prints out the command:

    alias oneliner='print -z $(grep "^(\*)" oneliners.txt | fzf -e | grep -oP "(?<=: \`).*(?=\`$)")'
    (requirements: zsh is your shell, GNU grep, fzf)
