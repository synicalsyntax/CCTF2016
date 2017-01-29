# Numbers (Forensics)

##About

Numbers was a challenge in the Forensics category worth 25 points. It was intended to be an easy challenge. 82 teams solved Numbers over the course of the competition.

##Description
"A picture is worth a thousand words."

###numbers.png
![](https://raw.githubusercontent.com/synicalsyntax/CCTF2016/master/forensics/numbers.png)

##Solution
We are given a PNG file. Any file from a challenge in the Forensics category should be first opened in a hex editor like HxD (or HexEdit for Mac) for binary analysis.

The next thing you should always do when given a file to examine is to check its [file signature](http://www.garykessler.net/library/file_sigs.html).

True to its name, this PNG file has the proper file signature with a header of 	**‰PNG....** or **89 50 4E 47 0D 0A 1A 0A** and a trailer of **IEND®B`‚...** or **49 45 4E 44 AE 42 60 82**.

However, something lies beyond the file trailer: **{y0u\_f0uNd\_th3\_1st\_p4rt** A part of the flag, perhaps?

![](https://raw.githubusercontent.com/synicalsyntax/CCTF2016/master/forensics/file.png)

As the string hints, the flag seems to be incomplete and we must find the second part of the flag.

Fortunately, the challenge description hints at us to look closer at the picture.... 95, 97, 78, 100, 95...

Could the numbers possibly indicate ASCII encryption? It's a high possibility.

After painstakingly examining the image, we get **\_aNd\_n0w\_y0u\_f0und\_th3\_oth3r}** as the last part of the flag. Concatenate the two strings together to get the flag.

Flag: **{y0u\_f0uNd\_th3\_1st\_p4rt\_aNd\_n0w\_y0u\_f0und\_th3\_oth3r}**
