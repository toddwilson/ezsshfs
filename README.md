ezsshfs
=======

Easy handling of multiple sshfs mounts

Depends on sshfs. Brew install it!

## Installation

* Create directory `~/.ezsshfs` (this is where your mount profiles will go)

* Add a new profile to the directory. Example:

```bash
# ~/.ezsshfs/example-profile

# leverage your ssh-config to do any special magic you need there
host="myhostname"

# What directory on the remote machine to mount to
host_dir="/"

# Local directory where the mount reside
local_dir="/Volumes/RemoteHost"
```

* Add `ezsshfs` to your $PATH



## Usage

Mount a SSHFS profile:

    $ ezsshfs start example-profile

Unmount:

    $ ezsshfs stop example-profile
