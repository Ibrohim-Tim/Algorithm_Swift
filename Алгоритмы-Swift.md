# Алгоритмы Swift
### Задача с перемещением 0 в конец массива 

```swift
 class Solution {
    func moveZeroes(_ nums: inout [Int]) {
        var nonZeroIndex = 0
        
        // Переместим все ненулевые элементы в начало массива
        for num in nums {
            if num != 0 {
                nums[nonZeroIndex] = num
                nonZeroIndex += 1
            }
        }
        
        // Заполним оставшуюся часть массива нулями
        while nonZeroIndex < nums.count {
            nums[nonZeroIndex] = 0
            nonZeroIndex += 1
        }
    }
}
```