---
title: "Data Structures And Algorithms Book"
date: 2022-10-18T16:56:59+13:00
draft: false
---

## Classification of data structures and design patterns

data structure - organization of data in a computers memory

Datatypes within a data structure 

(Heterogenous)
- Linked List.
- Ordered List.
- Unordered List.

(Homogenous)
Two dimensional arrays, multidimensional arrays

(Dynamic)
- dictionaries 
- tree sets 
- sequences

Linear Data Structures 
- lists
```
package main
import(
    "fmt"
    "container/list"
)

func main(){
    var inList list.list
    intList.pushBack(11)
    intList.pushBack(23)
    intList.pushBack(34)

    for element := intList.Front(); element != nil; element = element.Next(){
        fmt.PrintLn(element.Value.(int));
    } 
}


```


- sets
- tuples
- queues
- stacks 
- heaps

Non Linear
- Trees
- Tables
- Containers
