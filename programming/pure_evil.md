# Pure Evil (Programming)
##About
Pure Evil was a challenge in the Programming category worth 100 points. It was intended to be a mildly-difficult challenge; however, most participants found it easy to solve. 93 teams solved Basic Decryption over the course of the competition.

##Description
What is the sum of all ten-digit positive palindromic integers that have a factor of the first five-digit power of 2?

The flag is in the format {answer}.

##Solution
To solve this challenge, you must first ask yourself several questions, including "What is a palindrome?"

A palindrome, according to Wikipedia, "is a word, phrase, number, or other sequence of characters which reads the same backward or forward."

One easy way to solve this challenge is to realize that any ten-digit palindrome can be represented as a 5 letter numerical string concatenated by its reverse. Simply write a program that joins the string reverse of an integer variable and check if it's divisible by 16384, the first five-digit power of 2.

Example program in Python:
```python
x = 10000
sum = []
answer = 0

while x < 100000:
    y = str(x) + str(x)[::-1]
    if int(y) % 16384 == 0:
        sum.append(int(y))
    x = x + 1

for i in sum:
    answer = answer + i

print("{" + str(answer) + "}")
```

Example program in Javascript:
```javascript
var x = 10000;
var sum = [];
var answer = 0;

while (x < 100000) {
    y = x.toString() + x.toString().split("").reverse().join("");
    if (parseInt(y) % 16384 == 0) {
        sum.push(parseInt(y));
    }
    x++;
}

for (var i in sum) {
    answer = answer + sum[i];
}

console.log('{' + answer.toString() + '}');
```

This surely is not the most efficient way to solve this challenge (given all the string-integer conversions I'm doing), but it's a simple concept to understand and it works :)
