# Fundamental Command-Line skills


## How to view and change shells
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

## Differences between regular and administrative users:

Regular user: [victor@pc ~]$

Administrative user: [root@pc ~]#

## Command Redirection

Each file in Linux has a corresponding File Descriptor associated with it:
- Standard Input STDIN - File Descriptor: 0
- Standard Output STDOUT - File Descriptor: 1
- Standard Error STDERR - File Descriptor: 2
The keyboard is the standard input device while your screen is the standard output device:
- ">" is the output redirection operator. ">>" appends output to an existing file
- "<" is the input redirection operator
- ">&"re-directs output of one file to another.
- You can re-direct error using its corresponding File Descriptor 2.


## File searches:

- Find: Find depends on the memomry and disk speed available on the local system

- Locate: Sets up a database of installed files and directories. However is only updated once every every 24 hours as documented in the /etc/cron.daily/mlocate script. So run # /etc/cron.daily/mlocate on the exam to find the needed files.

## Commands to read text streams
- cat
- more
- Less command can read compressed files in .gz where as more and cat can't.
- head
- tail

## Commands to Process Text Streams
