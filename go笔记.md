## 将切片中的一个元素从索引`i`处移动到索引`j`
``` go
    k := a[i]
    copy(a[j+1:i+1], a[j:i])
    a[j] = k
    // 例子 i = 5, j = 3
    a := []int{8,4,6,7,3,2,1}
    k := a[i]  // 2
    copy(a[4:6], a[3:5]) // {3, 2} {7, 3}
    // a = {8, 4, 6, 7, 7, 3, 1}
    a[3] = k 
    // a = {8, 4, 6, 2, 7, 3, 1}
```