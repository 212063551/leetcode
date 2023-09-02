### 两数之和 
题目： 给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 target  的那 两个 整数，并返回它们的数组下标。

你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。

示例：
`输入：nums = [2,7,11,15], target = 9`
`输出：[0,1]`
`解释：因为 nums[0] + nums[1] == 9 ，返回 [0,1] `


######  解题思路 （ TypeScript ）

> map.has 是根据 key 来查询数组是否存在

1. 创建一个 [Map](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Map) 
   
2. for 循环遍历 nums 数组
   
3. 用 target 减 nums[i]
   *  计算哪个数能跟当前的数字相加得到target

4. 检查map里有没有这个数，
   * 如果有则返回结果，
   *  如果没有则把nums[i]们当作key，i 当作value放入map中（为什么？）
