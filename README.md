# device-sshd
Provides control over the SSH daemon.

This appliance does the following:

- All parameters passed to the device commands are syntax checked and canonicalised,
  with bash completion.
- Allows sshd server to be enable and disabled.
- Allows password authentication to be allowed or disallowed.

## before

- Deploy the device-sshd package.

```
[root@server ~]# dnf install device-sshd
```

## show configuration

To show the existing configuration, run show as follows.

```
[root@server ~]# device services sshd show
               disabled: no
password-authentication: no
```

## set password-authentication

To allow or disallow password authentication, run this. Possible options are "yes"
or "no".

```
[root@server ~]# device services sshd set password-authentication=no
```


