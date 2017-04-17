1. 让 IPAddr 类型实现 fmt.Stringer 以便用点分格式输出地址。
例如，IPAddr{1, 2, 3, 4} 应当输出 "1.2.3.4"。
``` go
package main

import "fmt"

type IPAddr [4]byte

// TODO: Add a "String() string" method to IPAddr.

func main() {
	addrs := map[string]IPAddr{
		"loopback":  {127, 0, 0, 1},
		"googleDNS": {8, 8, 8, 8},
	}
	for n, a := range addrs {
		fmt.Printf("%v: %v\n", n, a)
	}
}
```

2. 有下面的结构体，写一个通用反射调用方法，方法签名如下：
func callMethod(conf interface{}, method string, params []interface{}) []interface{} {}

``` go
type Conf struct {
	Op string
}

func (this Conf) SayOp(subName string, collection string) string {
	return this.Op + ":" + subName + ":" + collection
}

func main() {
	conf := Conf{}
	conf.Op = "create"
	ret := callMethod(&conf, "SayOp", []interface{}{"Db", "xx"})
	if reflect.TypeOf(ret[0]).Kind() == reflect.String {
		fmt.Printf("result: %s\n", ret[0])
	}
}
```