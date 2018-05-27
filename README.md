**Deprecated**

You should use [saltstack](https://saltstack.com).

autosshd for OSX
----------------
Provides a reverse ssh-tunnel with certificate-only authentication for remote
OSX admin rescue. This is intended for a poor-man's remote administration of
an OSX machine, without a large infastructure.

This will enable remote login (sshd) on boot, and ensure that an autossh
tunnel is maintained while the computer is on. It makes no attempt to hide the
tunnel in current processes.

Rescue Login
------------
Resue login can be done by connecting the reverse ssh-tunnel, if setup as
specified in CONFIG, like so:

ssh -p 50000 -i ~/.ssh/rescue-<MSN> rescue-<MSN>@localhost

Disabling
---------
Removing the LaunchDaemons will disable this software from working:

sudo launchctl unload /Library/LaunchDaemons/autossh*.plist

Installation
------------
Read CONFIG for how to configure on a OSX machine. Local ROOT access required.

Additional Downloads
--------------------
http://www.harding.motd.ca/autossh - The latest autossh source

http://developer.apple.com/downloads - CLI X-code tools installed (for compiling autossh)

