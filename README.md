# JavaScript Coding Challenges
As part of interview preparation I have worked on some javascript solutions for coding challenges and this repo will gather them.

---

> ## 1. Find duplicate
> Given an array of integers nums containing n + 1 integers where each integer is in the range [1, n] inclusive.
> There is only one repeated number in nums, return this repeated number.
> You must solve the problem without modifying the array nums and uses only constant extra space.
>
>
> ### Example 1:
> Input: nums = [1,3,4,2,2]
> Output: 2
> 
> ### Example 2:
> Input: nums = [3,1,3,4,2]
> Output: 3
>
> ### Example 3:
> Input: nums = [3,3,3,3,3]
> Output: 3
>
> ### Constraints:
> - 1 <= n <= 105
> - nums.length == n + 1
> - 1 <= nums[i] <= n
> - All the integers in nums appear only once except for precisely one integer which appears two or more times.
>
> 
> ```js
> var findDuplicate = function(nums) {
>    const inventario = {}
>       nums.forEach( num => {
>           if (inventario[num]){
>               inventario[num] += 1 
>           }
>           else {
>               inventario[num] = 1
>           }
>       })
>       
>       for (const [key, value] of Object.entries(inventario)) {
>           if (value > 1) return key
>       }
>   
> };
> ```
>




