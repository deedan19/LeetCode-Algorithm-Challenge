# LeetCode-Algorithm-Challenge

#### Search Insert
```swift
func searchInsert(_ nums: [Int], _ target: Int) -> Int {
    var checker = [Int]()
    var value = 0
    
    for index in 0..<nums.count {
        if nums[index] == target {
            value = index
        }
        
        if !nums.contains(target) {
            checker = nums
            checker.append(target)
        }
    }
    
    for indexValue in 0..<checker.sorted().count {
        if checker.sorted()[indexValue] == target {
            value = indexValue
        }
    }
    return value
}

searchInsert([1,3,5,6], 7)
```
