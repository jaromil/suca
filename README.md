# Super User Credential Authentication - SUCA

Notes on a new to innovate the way privilege escalation is done in
UNIX terminals, aka let's sweat it and beat sudo at it.

Starting point: https://sud.dyne.org

Licensing: Apache/MIT or BSD sort

## Components

Needs a small local database like [KISSDB](https://github.com/adamierymenko/kissdb) (or the kissdb-SGX fork?)

Needs secure string handline like [better string lib](https://github.com/msteinert/bstring) (fork of P. Hsieh)

Needs PAM or even better [https://github.com/skarnet/pamela](Pamela), if it works

Binary command executable analysis: symlink, permissions, hash, malware signature?
- https://github.com/gpakosz/whereami
- store hash in xattr https://man7.org/linux/man-pages/man2/setxattr.2.html
- hash may not need to be cryptographic https://cyan4973.github.io/xxHash/
- https://github.com/brandt/symlinks
- https://github.com/KubaKaszycki/symlink-track

Simple file based configuration (stb)

Password entry via pinentry - assuan protocol when available (gpg/libassuan)

Some more crypto (sign, hash) https://monocypher.org most likely not needed?

Good PAM implementation reference: https://github.com/Duncaen/OpenDoas/raw/master/pam.c

### XATTR signature:

```
HASH(64b):last-used(EPOCH):signature?
```



# Interested?

Gonna do it sometimes, but not alone. Mail J@dyne.org

