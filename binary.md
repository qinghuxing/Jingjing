>bin() to binary as string;

>a^b xor:

1^1 =0

1^0 =1

0^1 =1

0^0 =0

> [405]
1. (a>>4*i)&15 for i in range(8)
2. .lstrip('0')  delete all '0' from the left


> [371]
1. if I want a as a negative number, not a long type positive one:
mask=0xFFFFFFFF, return ~(a^mask)
2. ~a=-a-1

> [260]
a& ~(a-1), return the last '1' in the sequence of a. 


>x.zfill(32) fill with '0' at front to be 32 bits. x has to be string;
>'{:032b}'.format(x) same, x has to be interger.

