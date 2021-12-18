# 							Bit Manipulation

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

## 2. To divide a number by 2.

`n>>1` is known as the right shift operator, it divides the number `n` with 2.

Infact `n=n>>x` makes the value of `n=n/(2^x)` 



   
