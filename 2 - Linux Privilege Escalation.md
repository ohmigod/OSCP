# Linux Privilege Escalation

#### :red_circle: Upgrade shell
___
###### python:
```python
python -c 'import pty; pty.spawn("/bin/bash");'
```

###### bash:
```bash
SHELL=/bin/bash script -q /dev/null
Ctrl-Z
stty raw -echo
fg
reset
xterm
```

#### :red_circle: SUID binaries
___
```bash
find / -perm -u=s -type f 2>/dev/null
```

```bash
#printf shows the output with file(f), path(p), user(u), group(g) and permissions(m) in various columns (column -t):
find \ -perm -4000 -printf '%f\t%p\t%u\t%g\t%m\n' 2>/dev/null | column -t
#We can also specify the above command with a grep in order to see non root  SUID binaries:
find \ -perm -4000 -printf '%f\t%p\t%u\t%g\t%m\n' 2>/dev/null | column -t | grep -v "root"
```
