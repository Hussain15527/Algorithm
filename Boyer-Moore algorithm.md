#  Boyer-Moore algorithm

This algorithm is very useful in question where we need to find a majority element, (or question like, find the element which occur more than n/2 times, n being the size of the array).

*This post will assume that majority element always exist.*

### The Idea: (ME-->majority element):

we will choose first element as ME and set count to 1 

1.  if we encounter the same element as in the ME, we increment the count by 1.
2. if we encounter the different element as in the ME, we decrement the count by 1.
3. if the count=0, we change the ME as the current candidate element.

example:
nums = {2,2,1,1,1,2,2}

we start the with the 1st element, so the ME is nums[0]-->2 and count=1

Now we move to nums[1], it is same as ME, increase the count by 1(count==2).

since the nums[2]==1 which is not equal to the ME, we decrease the count by 1(count==1).

now we move to nums[3]==1 which is not equal to the ME, we decrease the count 1(count==0), since the count ==0 we update the ME, and set ME=1 and count==1.

nums[4]==1, which is equal to the ME, increase the count by 1(count==2).

nums[5]==2, which is not equal to the ME, decrease the count by 1(count==1).

nums[6]==2, which is not equal to the ME, decrease the count by 1(count==0), update ME as ME==nums[6]==2.

hence our answer is 2.

```java
public static int majorityElement(int[] nums) {
        int ME=nums[0];
        int count=1;
        for(int i=1;i<nums.length;i++){
            if(nums[i]==ME){
                count++;
            }else if(nums[i]!=ME){
                count--;
            }else if(count==0){
                ME=nums[i];
                count=1;
            }
        }return ME;
    }
```

