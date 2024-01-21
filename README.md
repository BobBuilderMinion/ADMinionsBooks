# Cracking

#### Zip password protected

````
```
zip2john winrm_backup.zip > zip.john
john zip.john -wordlist:/usr/share/wordlists/rockyou.txt
openssl pkcs12 -in legacyy_dev_auth.pfx -nocerts -out key.pem -nodes
python2 /usr/share/john/pfx2john.py legacyy_dev_auth.pfx > pfx.john
john pfx.john -wordlist:/usr/share/wordlists/rockyou.txt
openssl pkcs12 -in legacyy_dev_auth.pfx -nocerts -out key.pem -nodes
openssl pkcs12 -in legacyy_dev_auth.pfx -nokeys -out cert.pem
```
````

#### Net-ntlmv2:

````
```
.\hashcat.exe -m 5600 .\hashes.txt ../rockyou.txt
```
````

#### As-RepRoasting:

````
```
18200 = $krb5asrep$23$amber.smith@INLANEFREIGHT.LOCAL:3
```
````

#### Kerberoasting:

````
```
13100 = $krb5tgs$23$*ldap_monitor$REBOUND.HTB$ldap_monitor*$8d4a822
```
````

#### Kerberos ticket:

````
```
18200 = $krb5tgs$18$krbtgt$FLIGHT.HTB$*krbtgt*$a0ac8
```  
````
