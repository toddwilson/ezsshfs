ezsshfs
=======

Easy handling of multiple sshfs mounts

Installation
~~~~~~~~~~~~

1. Create directory `~/.ezsshfs` (this is where your mount profiles will go)

2. Add a new profile to the directory. Example:

    # ~/.ezsshfs/example-profile

    # leverage your ssh-config to do any special magic you need there
    host="myhostname"

    # What directory on the remote machine to mount to
    host_dir="/"

    # Local directory where the mount resides
    local_dir="/Volumes/RemoteHost"

3. Put `ezsshfs` in your $PATH

Usage
~~~~~

Mount a SSHFS profile:

    $ ezsshfs start example-profile

Unmount:

    $ ezsshfs stop example-profile