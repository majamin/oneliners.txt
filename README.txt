README.txt
----------

    This is a collection of oneliners, commands, scripts, etc. for UNIX-like systems.
    PRs are welcome - oneliners need to be in the format (see the file):

    (*) DESCRIPTION: `COMMAND`

    There are some non-oneliners. Not everything can be a oneliner.

How to find binaries for the commands in your distro
----------------------------------------------------

    You'll eventually get a 'command not found' message from your shell.
    You can try these commands to find the FILE (i.e. binaries) required to run some oneliners:

        Arch-based distros: `pacman -Fy FILE`
        Ubuntu-based distros: `apt-file update && apt-file find FILE`
        RHEL / CentOS-based distros: `yum whatprovides '*FILE'`
        Fedora: `dnf provides '*FILE'`
        OpenSUSE: `zypper wp FILE`

    For Windows, it's a dog's breakfast. With enough effort, similar commands
    can be ran there with mixed results (you're on your own).

    You can try installing `Mingw-w64` to start. It uses a port of `pacman` for installing packages:
        1. Open `Mingw-w64`
        2. Run `pacman -Syu` in the terminal so upgrade all packages.
        3. Repeat step 2 (closing and opening) until the commands reports "nothing to do".
        4. Run `pacman -Fyu FILE` to find a package containing the FILE.

TODO
----

    * Keep moving commandlinefu dump to organized categories.

Bonus
-----

    You can alias a simple command like this one to get a nice menu that prints out the command:

        alias oneliner='print -z $(grep "^(\*)" oneliners.txt | fzf -e | grep -oP "(?<=: \`).*(?=\`$)")'

    (requirements: zsh is your shell, GNU grep, fzf)
