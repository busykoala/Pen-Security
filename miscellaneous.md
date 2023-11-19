# Miscellaneous

References:

- [Forensics tools](https://www.hackingarticles.in/forensics-tools-kali/)
- [radare2 intro](https://insinuator.net/2016/08/reverse-engineering-with-radare2-intro/)
- [journey into radare2](https://www.megabeets.net/a-journey-into-radare-2-part-1/)

## John the Ripper

Password cracking

```bash
# linux users
unshadow /etc/passwd /etc/shadow > output.db
john output.db

# zip
zip2john file.zip > zip.hashes
john zip.hashes

# with some hashes in a text file (one per line)
john --format=raw-md5 --wordlist=dictionary.txt hash.txt
john --show hash.txt --format=raw-md5
```

## Metasploit

Metasploit is a powerful and widely used open-source framework for conducting
penetration testing and security research. It's designed to provide information
about security vulnerabilities and aid in the development and execution of
exploit code against a remote target machine.

## More

```bash
binwalk file  # show files in file
binwalk -e file  # extract files in file

file <file>  # get file infos
```
