oneliners.txt
-------------

    This is a collection of oneliners for UNIX-like systems.
    It's a dog's breakfast of compliance and dependencies (user beware!).
    Most lines are in the following format (SHELL is *nix by default):

    Format:

    ($) (SHELL) DESCRIPTION: `COMMAND`
      \    \
       \    \
        \   Specifies shell or *nix if blank
         \
         Can be run by regular user (# requires privileges)

Where's my command?
-------------------

    You might get a 'command not found' complaint from your shell.
    You can try your distro's corresponding command to find the package
    providing that CMD:

    Gentoo ............ `equery b $(which CMD)` (or `qfile`)
    Arch .............. `pacman -Fy CMD`
    Fedora ............ `dnf provides '*CMD'`
    Debian, Ubuntu .... `apt-file update && apt-file find CMD`
    RHEL / CentOS ..... `yum whatprovides '*CMD'`
    OpenSUSE .......... `zypper wp CMD`
    Powershell ........  (no standard way: try `Get-Help CMD`)
