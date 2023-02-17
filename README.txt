oneliners.txt
-------------

    This is a collection of oneliners, commands, scripts, etc. for UNIX-like systems.
    Some Powershell commands are also included. Most lines are in this format:

    ($) (SHELL) DESCRIPTION: `COMMAND`

Notes
-----

    (#) Show only errors and warnings: `dmesg --level=err,warn`
      \
       \
        \
       This command will probably require elevated privileges (`sudo`, etc.)

    ($) (Powershell) Change directory (`cd` works as well): `Set-Location .\mydir`
           \
            \
             \
            The command is suitable in this shell only.

Command not found
-----------------

    You'll eventually get a 'command not found' complaint from your shell.
    You can try these commands to find the FILE (i.e. binaries) required to run some oneliners:

        Gentoo: `equery b $(which FILE)` (`qfile` is another possibility)
        Arch-based distros: `pacman -Fy FILE`
        Ubuntu-based distros: `apt-file update && apt-file find FILE`
        RHEL / CentOS-based distros: `yum whatprovides '*FILE'`
        Fedora: `dnf provides '*FILE'`
        OpenSUSE: `zypper wp FILE`

    If you like your *NIX, but you're using Windows, you can install MSYS2 or WSL to get many (but not all) of the commands listed.
    Analogs of *NIX commands exist in Powershell, and a few are listed as examples (with 'unixy' translations).
