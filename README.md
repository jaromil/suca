# Super User Credential Authentication - SUCA

This project is just a wish for now and it collects notes on how to code a better software to do privilege escalation in
any POSIX system.

The starting point: https://sud.dyne.org

The licensing: Apache/MIT or BSD sort

## Selected components

Needs a small local database like [KISSDB](https://github.com/adamierymenko/kissdb) (or the kissdb-SGX fork?)

Needs secure string handline like [better string lib](https://github.com/msteinert/bstring) (fork of P. Hsieh)

Needs to use [https://github.com/skarnet/pamela](Pamela) for PAM functions, from Skarnet

Binary command executable analysis: symlink, permissions, hash, malware signature?
- https://github.com/gpakosz/whereami
- store hash in xattr https://man7.org/linux/man-pages/man2/setxattr.2.html
- hash may not need to be cryptographic https://cyan4973.github.io/xxHash/
- https://github.com/brandt/symlinks
- https://github.com/KubaKaszycki/symlink-track

Simple file based configuration (stb)

Password entry via pinentry - assuan protocol when available (gpg/libassuan)

## Docs

Good PAM implementation reference: https://github.com/Duncaen/OpenDoas/raw/master/pam.c

XATTR signature:
```
HASH(64b):last-used(EPOCH):signature?
```



# Interested?

Gonna do it sometimes, but not alone. If interested mail me at J@dyne.org

