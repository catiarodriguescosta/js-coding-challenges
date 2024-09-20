# JavaScript Coding Challenges
As part of interview preparation I have worked on some javascript solutions for coding challenges and this repo will gather them.

---

> ## 01. Find duplicate
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

---

>
> ## 02. Birthday on fridays/weekend until 2050?
>
>```js
>
>function run(birthday_date) {
>	const initialYear = 2016
>	const finalYear = 2050	
>	const weekDays=["Mon", "Tues", "Wed", "Thur", "Fri", "Sat", "Sun"]
>	future_dates = ""
>
>	const d = birthday_date.split("-")[0]
>	const m = birthday_date.split("-")[1]
>
>	for (let y = initialYear; y<= finalYear; y++) {
>     const dd = y+"-"+m+"-"+d
>		const bdate = new Date(dd)
>		if (bdate.getDay() > 4) {
>     future_dates += " "+ y + ": "+ weekDays[ bdate.getDay() -1 ]+","
>		}
>	}
>	// to remove the first space
>	if (future_dates !== null) {
>      future_dates = future_dates.substring(1)
>    }
>	
>	return future_dates;
>}
>
>console.log(run("11-10"))
> // 2019: Fri, 2024: Fri, 2025: Sat, 2030: Fri, 2031: Sat, 2036: Sat, 2041: Fri, 2042: Sat, 2047: Fri,
>```




