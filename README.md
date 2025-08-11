### golang sdk不用打包，直接在github上面引用就行了。
直接import就行了。
import (
	"fmt"
	"github.com/zhuhuanchen/my-sdk"
)


测试代码
```
package main

import (
	"fmt"
	"github.com/zhuhuanchen/my-sdk"
)

func main() {
	//client := mysdk.NewClient("https://api.example.com", "my-api-key")
	client := mysdk.NewClient("https://jsonplaceholder.typicode.com", "")

	data, err := client.GetData("/users")
	if err != nil {
		panic(err)
	}
	fmt.Println("API Response:", data)
}
```
