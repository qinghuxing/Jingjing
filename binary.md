>. 1 byte= 8 bits= 0x00 ~ OxFF =0 ~ 255

...

> [477] Calculate the total hamming distance in one list;

1. At the particular bit, count the number of '1's and number '0's, and let the number of '1's times the number of '0's;
2. sum the result for all the bits
3. remember 2^31 = 2.147483648 * 2^10;

> [421] Maximum XOR of two numbers in a list;

1. start from the first bit;
2. 1^num to see if it is still in the **set** of the list, for num in list;
3. if yes, that bit can be '1', or it is '0';

> [318*] Maximum product of word lengths where the two word don't have same character;

1. see if two words have same character
```
a=0;
for i in set(word_1):
      a|=(1<<(ord(i)-ord('a')));
b=0;
for i in set(word_2):
      b|=(1<<(ord(i)-ord('a')));
return not a&b    
```
2. set a dict to store the relation of integer value and length

> [136][137][260] Find the single number(s) in a list;

1. a^a^x=x; XOR is good to reduce the words repeat twice;
2. If the words repeat more than twice, set a state transfer rule to make it work;
3. if the single word is not unique, set corresponding groups where in each group there is only one unique word.





> [405]

1. change Integer a to hex,
```
(a>>4*i)&15 for i in range(8)
```
2. .lstrip('0')  delete all '0' from the left

> [371]

1. if I want a as a negative number, not a long type positive one:
mask=0xFFFFFFFF, return ~(a^mask)
2. ~a=-a-1, a>=0

> [260]

a& ~(a-1), return the last '1' in the sequence of a as '1000..0'



>x.zfill(32) fill with '0' at front to be 32 bits. x has to be string;

>'{:032b}'.format(x) same, x has to be interger.
