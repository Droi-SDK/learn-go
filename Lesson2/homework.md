
##习题1  

使用移位运算和循环结构模拟数据移位的过程，打印如下结果：  

    00000001
    00000010
    00000100
    00001000
    00010000
    00100000
    01000000
    10000000

##习题2  

以下执行结果为多少  

    package main
    
    import (
    	"fmt"
    )
    
    const (
    	a = "a"
    	b
    	c = iota
    	d = c
    	e
    )
    
    const (
    	f = b
    	g = iota
    )
    
    func main() {
    	fmt.Println(a)
    	fmt.Println(b)
    	fmt.Println(c)
    	fmt.Println(d)
    	fmt.Println(e)
    	fmt.Println(f)
    	fmt.Println(g)
    }

##习题3

以下程序打印1-7，有哪些错误：

    package main
    
    var max uint32 = 10
    var i int
    
    func main() {
    LABEL:
    	for {
    		break LABEL
    	}
    
    	for i= 0; i <= max{
    		switch i++ {
    		case 1,2:
    		case 3,4,5,6,7:
    			fmt.Println(i)
    		}
    
    		if i >= 7 {
    			break LABEL
    		}
    	}
    }

##习题4

以下运算的结果  

    package main
    
    import "fmt"
    
    func main() {
    	var v = 9 &^ 5 << 4
    	var c int8 = int8(v)
    	fmt.Println(c)
    }



