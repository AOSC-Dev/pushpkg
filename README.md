pushpkg
===

A simple wrapper script for the standard AOSC OS package upload procedure.

You should run this script inside a directory which contains a `debs` directory.

Usage
---

```
usage: pushpkg [-h] [-v] [-d] [-f] [-r] [-6] [-4] [-C] [--host [HOST]] [-i IDENTITY_FILE] [--allow-marking-upload-done-to-fail] [USERNAME] [BRANCH] [COMPONENT]

pushpkg, push aosc package to repo.aosc.io or mirrors

positional arguments:
  USERNAME              Your LDAP username.
  BRANCH                AOSC OS update branch (stable, stable-proposed, testing, etc.)
  COMPONENT             (Optional) Repository component (main, bsp-sunxi, etc.) Falls back to "main" if not specified.

options:
  -h, --help            show this help message and exit
  -v, --verbose         Enable verbose logging for ssh and rsync
  -d, --delete          Clean OUTPUT directory after finishing uploading.
  -f, --force-push-noarch-package
                        Force Push noarch package.
  -r, --retro           Push to AOSC OS/Retro repo
  -6, --ipv6            Use IPv6 addresses only
  -4, --ipv4            Use IPv4 addresses only
  -C, --compress        Requests compression of all data for SSH, note this option should be used with caution
  --host [HOST]         Specify the rsync host to push packages, defaults to repo.aosc.io
  -i IDENTITY_FILE, --identity-file IDENTITY_FILE
                        SSH identity file
  --allow-marking-upload-done-to-fail
                        Allow marking upload as done to fail
```
