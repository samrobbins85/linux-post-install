# Errors

Use this document when you encounter a problem, it might help

### Flatpak/Snap applications aren't opening, saying they can't open the display

If you've changed the hostname recently, this may be the culprit.

It can be verified if this is the problem by running the two commands

```bash
echo $XAUTHLOCALHOSTNAME
hostname
```

If they are both the same, then it's a different problem, good luck :(

If they are different, run the command

```bash
hostnamectl --static set-hostname [Hostname]
```

Replacing [Hostname] with your hostname and this should work
