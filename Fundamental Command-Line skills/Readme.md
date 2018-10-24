
- To view the shells installed on your system run:
  - cat /etc/shells
- To know which one you are using run:
  - grep youruser /etc/passwd
- To change your bash run
  - chsh --shell /bin/tcsh (for example)

chsh is a command to change shell

You can use up to 6 virtual terminals to open six independent login sessions. However, only one virtual terminar is activated by default. The others are launched dinamically when you switch to an unused terminal.
Virtual directories are defined by the logind.conf file in /etc/systemd directory in an option called NAutoVts which defines the maximum number of virtual terminals that can be activated. 
It's possible to configure more virtual terminals limited by those allowed for the root administrative user in /etc/securetty file.

Differences between regular and administrative users:

Regular user: [victor@pc ~]$ 
Administrative user: [root@pc ~]#
