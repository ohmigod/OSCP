# Service Enumeration

>There are a variety of services running on so many systems…take the time to understand them! Do not just scan them and move on. Take some time to look at each of them because they could be a key for you to obtain shell access on a system!

[Cheatsheet1](http://0daysecurity.com/penetration-testing/enumeration.html)

[Cheatsheet2](https://highon.coffee/blog/penetration-testing-tools-cheat-sheet/)

______
#### :red_circle: NFS ENUM

>

**Check if any share is available:**

```bash
showmount -e $IPADDRESS
```

**If this command outputs any shares, try to mount it:**

______
