# findmyhash

![](https://storage.googleapis.com/google-code-archive/v2/code.google.com/findmyhash/logo.png)

Python script to crack hashes using online services

## Original Repository

https://code.google.com/archive/p/findmyhash/

## findmyhash.py
findmyhash.py try to crack different types of hashes using free online services.

**NOTE: findmyhash.py is out of date.**

## findmyhash.py 1.1.2

### Usage
```
python findmyhash.py algorithm OPTIONS
```

### Accepted algorithms are

* MD4 - RFC 1320
* MD5 - RFC 1321
* SHA1 - RFC 3174 (FIPS 180-3)
* SHA224 - RFC 3874 (FIPS 180-3)
* SHA256 - FIPS 180-3
* SHA384 - FIPS 180-3
* SHA512 - FIPS 180-3
* RMD160 - RFC 2857
* GOST - RFC 5831
* WHIRLPOOL - ISO/IEC 10118-3:2004
* LM - Microsoft Windows hash
* NTLM - Microsoft Windows hash
* MYSQL - MySQL 3, 4, 5 hash
* CISCO7 - Cisco IOS type 7 encrypted passwords
* JUNIPER - Juniper Networks $9$ encrypted passwords
* LDAP_MD5 - MD5 Base64 encoded
* LDAP_SHA1 - SHA1 Base64 encoded

### Valid OPTIONS are

```
-h hash_value: If you only want to crack one hash, specify its value with this option.

-f file: If you have several hashes, you can specify a file with one hash per line.

NOTE: All of them have to be the same type.

-g: If your hash cannot be cracked, search it in Google and show all the results.

NOTE: This option ONLY works with -h (one hash input) option.
```

### Examples

* Try to crack only one hash. 

```
$ python findmyhash.py MD5 -h "098f6bcd4621d373cade4e832627b4f6"
```

* If the hash cannot be cracked, it will be searched in Google.
```
$ python findmyhash.py SHA1 -h "A94A8FE5CCB19BA61C4C0873D391E987982FBBD3" -g
```

* Try to crack all the hashes of a file (one hash per line).
```
$ python findmyhash.py MYSQL -f mysqlhashesfile.txt
```

### More examples: 

```
$ python findmyhash.py MD4 -h "db346d691d7acc4dc2625db19f9e3f52" 
$ python findmyhash.py MD5 -h "098f6bcd4621d373cade4e832627b4f6" 
$ python findmyhash.py SHA1 -h "a94a8fe5ccb19ba61c4c0873d391e987982fbbd3" 
$ python findmyhash.py SHA224 -h "90a3ed9e32b2aaf4c61c410eb925426119e1a9dc53d4286ade99a809" 
$ python findmyhash.py SHA256 -h "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08" 
$ python findmyhash.py SHA384 -h "768412320f7b0aa5812fce428dc4706b3cae50e02a64caa16a782249bfe8efc4b7ef1ccb126255d196047dfedf17a0a9" 
$ python findmyhash.py SHA512 -h "ee26b0dd4af7e749aa1a8ee3c10ae9923f618980772e473f8819a5d4940e0db27ac185f8a0e1d5f84f88bc887fd67b143732c304cc5fa9ad8e6f57f50028a8ff" 
$ python findmyhash.py RMD160 -h "5e52fee47e6b070565f74372468cdc699de89107" python findmyhash.py GOST -h "a6e1acdd0cc7e00d02b90bccb2e21892289d1e93f622b8760cb0e076def1f42b" 
$ python findmyhash.py WHIRLPOOL -h "b913d5bbb8e461c2c5961cbe0edcdadfd29f068225ceb37da6defcf89849368f8c6c2eb6a4c4ac75775d032a0ecfdfe8550573062b653fe92fc7b8fb3b7be8d6" 
$ python findmyhash.py LM -h "01fc5a6be7bc6929aad3b435b51404ee:0cb6948805f797bf2a82807973b89537" 
$ python findmyhash.py LM -h "01fc5a6be7bc6929aad3b435b51404ee" 
$ python findmyhash.py NTLM -h "01fc5a6be7bc6929aad3b435b51404ee:0cb6948805f797bf2a82807973b89537" 
$ python findmyhash.py NTLM -h "0cb6948805f797bf2a82807973b89537" 
$ python findmyhash.py MYSQL -h "378b243e220ca493" 
$ python findmyhash.py MYSQL -h "*94bdcebe19083ce2a1f959fd02f964c7af4cfc29" 
$ python findmyhash.py MYSQL -h "94bdcebe19083ce2a1f959fd02f964c7af4cfc29" 
$ python findmyhash.py CISCO7 -h "12090404011C03162E" 
$ python findmyhash.py JUNIPER -h "\$9\$90m6AO1EcyKWLhcYgaZji" 
$ python findmyhash.py LDAP_MD5 -h "{MD5}CY9rzUYh03PK3k6DJie09g==" 
$ python findmyhash.py LDAP_SHA1 -h "{SHA}qUqP5cyxm6YcTAhz05Hph5gvu9M="
```

# Contact
Web: http://laxmarcaellugar.blogspot.com/

Mail/Google+: bloglaxmarcaellugar AT gmail DOT com

twitter: @laXmarcaellugar

# Acknowledgements
* Paul Sherman for the findmyhash logo - http://www.wpclipart.com/
* Zen Vantalye for the patch will be published really soon
