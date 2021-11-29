# Brian Kernighan’s algorithm(number of set bit)

It is a better algorithm than the usual method where we check whether the rigth most bit is set or not and then we do n>>1, to make to second bit the last bit and continue the process. 



Brain kernighan's algorithm does the same but with better efficiency.

The idea is that and number n and n-1 has a certain similarity.
Let the number n=10

n     =  10  -->  10**10**
n-1  =    9  -->  10**01**

Focus on the bit containing the right most set bit and all the bits after that. **they have been flipped** (0 became 1 and 1 became 0).

Now observe what happens when we take *bitwise* `and` of n and n-1.

n&(n-1)  -->  10**00** 

Note what happened to the *previous* right most bit and all the bit after that. **they have all been converted to 0**

Now the number **n** becomes decimal of **(n&(n-1))** i.e 1000 which converets to **8**

we repeat the process till the number n becomes **0**, also at every point it un-set the previous set bit, therefore, number of times it runs is equal to the number of set bit it has..

```java
static int set_bit(int n){
    //variable that counts the number of set bit
    int count = 0;
	while (n != 0) {
        //at each step the value of n changes such that all the numbers from right most set bit is changed to 0 including the right most set bit.
        n = n & (n - 1);
        //number of times this loop will run is equals to the number of set bit, therefore at each step the counter variable is increased.
        count++;
    }
    return count;
}
```







 