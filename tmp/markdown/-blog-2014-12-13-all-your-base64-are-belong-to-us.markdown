I recently found the [Matasano Crypto
Challenges](http://cryptopals.com/) and eagerly set about solving the
first one - converting a hex string to base64.

<!-- more -->

Hex (short for hexadecimal) is the base 16 number system, so whereas
decimal has 10 symbols representing the values from 0 to 9, hexadecimal
has 16 representing the values 0 to 15. It uses the numbers 0-9 for 0-9
and then the letters a-f for 10-15. Base64 on the other hand has 64
symbols representing the values 0 to 63 (A-Z representing 0-25, a-z
representing 26-51, 0-9 representing 52-61 and + and / representing 62
and 63 respectively)

Any number can be represented in any base as a polynomial. For example
we can represent any number, \\(N\_{16}\\) in base 16 (hexadecimal) as
the following:

\\[ \sum*{i} a*{i} 16\^i \\]
