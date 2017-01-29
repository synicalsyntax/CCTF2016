# Basic Decryption (Cryptography)
##About

Basic Decryption was a challenge in the Cryptography category worth 25 points. It was intended to be an easy challenge; however, most participants found it challenging. Only 29 teams solved Basic Decryption over the course of the competition.

##Description
This should be easy.

###basic_decyption.txt
```
JVWVK2DCK5MXQS3LIZBE2Q3TFNLVO5BQJVVVKN3CKR3XQUSWPBIVUU3TFNSFG53KJVVWY23BNVGXQWKTJJRU6Q3TF5FW2ZCTJVCTSMKPNR2ECTL2GRTWKMTHGBGVOWRTLFMGYZTEI5TXUY3NKY4Q
```

##Solution

The text file contains the following string:

```
JVWVK2DCK5MXQS3LIZBE2Q3TFNLVO5BQJVVVKN3CKR3XQUSWPBIVUU3TFNSFG53KJVVWY23BNVGXQWKTJJRU6Q3TF5FW2ZCTJVCTSMKPNR2ECTL2GRTWKMTHGBGVOWRTLFMGYZTEI5TXUY3NKY4Q
```

You'll recognize it as being encrypted in Base32. Decryption produces the following string:

```
MmUhbWYxKkFBMCs+WWt0MkU7bTwxRVxQZSs+dSwjMklkamMxYSJcOCs/KmdSME91OltAMz4ge2g0MWZ3YXlfdGgzcmV9
```

That's Base64. Decryption gets you:

```
2e!mf1*AA0+>Ykt2E;m<1E\Pe+>u,#2Idjc1a"\8+?*gR0Ou:[@3> {h41fway_th3re}
```

That was encrypted with Ascii85. Use a brain and delete the fake flag. Then you get:

```
7b 62 34 35 69 63 5f 66 6c 34 67 7d 0d 0a
```

Decrypting the encrypted hexadecimal gets you the flag: **{b45ic_fl4g}**
