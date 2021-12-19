# 							Usefull observations:

## 1. To check wheter a number is odd or even.

`If n&1==0` --> the number n is even
`If n&1==1` --> the number n is odd

we can clearly observe that every even number has `0` as the right most bit therefore if we take it's `and` with `1` then the resulting number will become `0`. 

ex. 4-->100 and 1-->001, 
  100
&001
*------*
  000

In the same way it can be proven that evey odd number ends with `1` as it's right most bit, therefore it's `and` with `1` gives `1` as the result.

## 2. To divide a number by 2 (or divide by 2^i, where 0<=i<= any number).

`n>>1` is known as the right shift operator, it divides the number `n` with 2.

Infact `n=n>>x` makes the value of `n=n/(2^x)` 

## 3. Xor observation.

### A) 

 **If `n` is `even` then `n^(n+1)==1` **

ex.`n=6`, `bin(n)=110` and `bin(n+1)=111`, we can observe that if `n` is an `even` then then difference between binary representation of `n`and `n+1` is just the right most bit rest all the bits are same, and we know that in `xor` operation only different bit result in `1` and same bit result in `0`, therefore in the above case, only right most bit is `1`.

### B)

**If `n%4==0`, then `n^(n+2)=2` ** 

ex. `n=4,` `bin(n)=100` and `bin(n+2)==110` , we can observe that only second bit from the right is different, all other bits are same, therfore if we take `xor` of `n` and `n+2` it will result in `2`.





   