# Table of content
## Array section
1. Two numbers
  - 空间换时间，创建一个新数组用来存储原数组的value和index
  - 遍历原数组中每一个value，查找index等于（target-value）的元素是否存在，如存在直接返回新数组中该index的值，不存在则插入
  - 收获：
    - 空间复杂度O(n),线性关系
    - 时间复杂度O(1),O(logN),O(n),O(n)^2,依次为增加，其中O(1)是指当数组元素足够多的时候，计算时间约等于一个常量，o(n)是指和给定参数线性相关，o(logn)是给定参数的开方，o(n)^2是与给定参数的平方相关
2. Remove duplicate numbers in a sorted array
  - 思路1:遍历数组，如果两个相邻数字相等，就调用array.slice(parm1,parm2),其中parm1是第一个相同数字的下标，parm2=1，这样就删除了重复的数字，并且符合题目要求，在原数组改动，不新建新数组
  - 思路2: 由于数组是排序过的，所以引入两个指针i 和j，i从头到尾遍历数组（慢指针），当nums[i]=nums[j]，i右移直到num[i]!=nums[j]的时候，说明重复的数字结束了，这时候把nums[i]的值记录到nums[j+1]里面,最后返回j+1即为结果
> var removeDuplicates = function(nums) {
     var k = 0;
    for (var i = 1; i < nums.length; i ++) {
        if (nums[i] > nums[k]) {
            nums [++k] = nums[i];
        }
    }
    return k+1;
};


- Reverse Integer   
- Palindrome Number   
