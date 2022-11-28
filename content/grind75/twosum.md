---
title: "Grind 75 -Two Sum"
date: 2022-10-18T16:56:59+13:00
draft: true
---

1. two sum solution 

```
func twoSum(nums []int, target int) []int {

	indices := [][]int{}

	for i := 0; i < len(nums); i++ {
		for j := i; j < len(nums); j++ {
			if nums[i]+nums[j] == target {
                if i != j {
				     indices = append(indices, []int{i, j})
                }
            }
		}
	}

    fmt.Println(indices)		
	return indices[0]
}
```

