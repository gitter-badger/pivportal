pam_pivportal
==================


Build
====

```bash
$ make
```

Install
====

```bash
$ make install
```

Example /etc/pam.d/sudo file:

```bash
auth required pam_pivportal.so
account include system-auth
password include system-auth
session optional pam_keyinit.so revoke
session required pam_limits.so
```