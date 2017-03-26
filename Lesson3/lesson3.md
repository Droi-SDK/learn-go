## 课堂练习
1. 有一个数组a [5]int{1, 2, 3, 4, 5}，需要通过循环打印出如下的：(提示：使用slice)  
   [[1 2 3 4 5] [2 3 4 5 1] [3 4 5 1 2] [4 5 1 2 3] [5 1 2 3 4]]
``` go
package main

import "fmt"

func main() {
	a := [5]int{1, 2, 3, 4, 5}
	// 修改这里
}
 ```

2. 实现 WordCount。它应当返回一个含有 s 中每个 “词” 个数的 map。函数 wc.Test 针对这个函数执行一个测试用例，并输出成功还是失败。  
需要使用到[strings.Fields](https://go-zh.org/pkg/strings/#Fields)
``` go
package main

import (
	"golang.org/x/tour/wc"
)

func WordCount(s string) map[string]int {
    //修改这里
}

func main() {
	wc.Test(WordCount)
}
```
