# WEB Enumeration

#### :red_circle: Vulnerability Scanner
_____
##### Nikto:
```bash
nikto -h $URL
```

##### dirb:
```bash
dirb $URL $WORDLIST_PATH
```

#### :red_circle: WordPress Scanner

```bash
wpscan --url $URL -e $ENUM_OPTIONS
#Separate options by comma
```

Enum options:

| **Option** | **Description**                            |
|------------|--------------------------------------------|
|vp          | Vulnerable plugins                         |
|ap          | All plugins                                |
|vt          | Vulnerable themes                          |
|at          | All themes                                 |



_____

## WFUZZ

#### Bruteforce subdomains using WFUZZ:
```bash
#WFUZZ is the word to change in the brute force mechanishm
#-c stands for colorized output
#--hc stands for Hide Code.
wfuzz -c --hc=404 -w $WORDLIST http://WFUZZ.$DOMAIN.$TLD
```

#### Broceforce hidden folders using WFUZZ:
```bash
wfuzz -c --hc=404 -w $WORDLIST http://.$DOMAIN.$TLD/WFUZZ
```
