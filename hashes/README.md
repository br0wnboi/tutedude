# This section contains practice hashes for you to crack.


> ### One line to rule them all: `sth -f hashfile`

### Recommended resources:

||Name|Link|Usage|
|-----|-----|-----|----|
|1|Crackstation|[Website](https://crackstation.net) | [Click here](#1-crackstation) |
|2|Search That Hash|[Github](https://github.com/HashPals/Search-That-Hash) | [Click here](#2-search-that-hash) |
|3|Hashcat|[Website](https://hashcat.net/hashcat/) | [Click here](#3-hashcat) |
|4|John The Ripper|[Website](https://www.openwall.com/john/) | [Click here](#4-john-the-ripper) |
|5| Hashid | [Website](https://psypanda.github.io/hashID/) | [Click here](#5-hashid) |

### Usage:
#### 1. Crackstation

Visit the website crackstation.net
Paste your line seperated hashes in the box
Complete Captcha
Click on crack hashes

----

#### 2. Search that hash

- Open line seperated hashes file
```bash
sth -f hash.txt
```
- Crack single hash
```bash
sth -t "hash-here"
```

-----

#### 3. Hashcat

`hashcat -a 0 -m 400 example400.hash example.dict`<br>
Where:<br>
`-a` uses Straight mode<br>
`-m 0` defines which mode to use, 0 is for MD5 <br>
`example.hash` is your hashfile<br>
`example.dic` is your bruteforce dictionary, mostly _rockyou.txt_<br>

-----

#### 4. John the Ripper
`john --format=raw-md5 --wordlist=example.dic example.hash`<br>
Where:<br>
`--format=MD5` defines the hash format as MD5<br>
`--wordlist=example.dic` defines the dictionary file to use for cracking, mostly _rockyou.txt_<br>

-----
#### 5. Hashid
`hashid -m -j -o hashid.txt enteryourhashhere`<br>
Where:<br>
`-m` shows corresponding mode in hashcat<br>
`-j` shows corresponding mode in john<br>
`-o` saves the output to a specified file<br>