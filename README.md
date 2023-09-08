# majka

"Free natural language morphology pack for debian"

Majka is very fast (approx. 1M words per second) free morphological analyzer Majka including databases for Czech, Slovak, Polish, Swedish, German, French, Italian, English, Portuguese, Catalan, Welsh, Spanish, Galician, Asturian and Russian. 

# Usage

Program expects one entry (word, lemma, or string lemma:tag, according the data file in use) per line on its standard input and prints the requested information on its standard output. An example of usage (for other options see majka -h):

```shell
$ echo test | majka -f /usr/lib/majka/majka.w-lt
test:k1gInSc1
test:k1gInSc4
test:k1gMnSc1
testa:k1gFnPc2
```

## Installation

There is Debian repository with packages for amd64, armhf, aarch64 architectures:

```shell
sudo apt install lsb-release wget apt-transport-https bzip2
wget -qO- https://repo.vitexsoftware.com/keyring.gpg | sudo tee /etc/apt/trusted.gpg.d/vitexsoftware.gpg
echo "deb [signed-by=/etc/apt/trusted.gpg.d/vitexsoftware.gpg]  https://repo.vitexsoftware.com  $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/vitexsoftware.list
sudo apt update

sudo apt install majka
```

```shell
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  majka
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 13.4 MB of archives.
After this operation, 32.0 MB of additional disk space will be used.
Get:1 http://repo.vitexsoftware.com bullseye/main armhf majka armhf 2016.1.22 [13.4 MB]
Fetched 13.4 MB in 2s (6,849 kB/s)
Selecting previously unselected package majka.
(Reading database ... 55925 files and directories currently installed.)
Preparing to unpack .../majka_2016.1.22_armhf.deb ...
Unpacking majka (2016.1.22) ...
Setting up majka (2016.1.22) ...
Processing triggers for libc-bin (2.31-13+rpt2+rpi1+deb11u5) ...
```

Package install data files into **/usr/lib/majka/**

```shell
vitex@glencoe:~ $ ls -la /usr/lib/majka/
total 31220
drwxr-xr-x  2 root root    4096 Sep  8 23:41 .
drwxr-xr-x 75 root root    4096 Sep  8 23:41 ..
-rw-r--r--  1 root root  642708 Apr  1  2015 majka.lt-w
-rw-r--r--  1 root root  509340 Apr  1  2015 majka.l-wt
-rw-r--r--  1 root root 1065180 Jan 22  2016 majka.w-lt
-rw-r--r--  1 root root  285510 Jul 29  2014 w-lt.as.fsa
-rw-r--r--  1 root root  641874 Jul 29  2014 w-lt.ca.fsa
-rw-r--r--  1 root root 3940549 Jul 29  2014 w-lt.cy.fsa
-rw-r--r--  1 root root  244776 Aug  1  2014 w-lt.en.fsa
-rw-r--r--  1 root root  621250 Jul 29  2014 w-lt.es.fsa
-rw-r--r--  1 root root  901142 Jul 29  2014 w-lt.fr.fsa
-rw-r--r--  1 root root 4868960 Jul 29  2014 w-lt.ger.fsa
-rw-r--r--  1 root root  401046 Jul 29  2014 w-lt.gl.fsa
-rw-r--r--  1 root root  492230 Jul 29  2014 w-lt.it.fsa
-rw-r--r--  1 root root 3263451 Feb 25  2014 w-lt.pl.fsa
-rw-r--r--  1 root root  800258 Jul 29  2014 w-lt.pt.fsa
-rw-r--r--  1 root root 3639972 Jul 29  2014 w-lt.ru.fsa
-rw-r--r--  1 root root 8998685 Jan 24  2016 w-lt.sk.fsa
-rw-r--r--  1 root root  611744 Jul 29  2014 w-lt.swe.fsa
```

## Author 

>  **Pavel Šmerk, Ph.D.**
> 
>  ma@nlp.fi.muni.cz
> 
>  Natural Language Processing Centre
> 
>  Faculty of Informatics, Masaryk University
> 
>  Botanická 68a, 602 00, Brno, Czech Republic
> 

[https://nlp.fi.muni.cz/ma/](https://nlp.fi.muni.cz/ma/)
