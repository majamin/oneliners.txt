oneliners.txt
-------------

    This is a collection of oneliners, commands, scripts, etc. for UNIX-like systems.
    Some Powershell commands are also included. Most lines are in this format:

    (*) DESCRIPTION: `COMMAND`

    (*) (SU) Show only errors and warnings: `dmesg --level=err,warn`
          ▲
          ▲
          ▲
    Some lines have a descriptor if they refer to a specific OS, or usage (such as superuser).

Command not found
-----------------

    You'll eventually get a 'command not found' message from your shell.
    You can try these commands to find the FILE (i.e. binaries) required to run some oneliners:

        Arch-based distros: `pacman -Fy FILE`
        Ubuntu-based distros: `apt-file update && apt-file find FILE`
        RHEL / CentOS-based distros: `yum whatprovides '*FILE'`
        Fedora: `dnf provides '*FILE'`
        OpenSUSE: `zypper wp FILE`

    In Windows, you can install MSYS2 or WSL to get similar *NIX-like commands.
    You can use 'chocolatey' to get some binaries, or perhaps just learn Powershell
    to do many of the things typically possible on *NIX systems (some PS commands
    are included in this repo!)
