## 使用 
- 注意代码前缀
	- http://localhost:8080/prefix/debug/pprof/profile
	- `wget http://localhost:8080/debug/pprof/profile`


## 本地测试
无论是命令行模式的`list`命令还是浏览器模式的`source`页面，为了查看指标消耗具体在哪一行，都需要源代码。但是当实际程序是在远端编译（线上程序）或者程序的源代码目录变了，则 pprof 从原路径找不源代码，那么就没法看到消耗在哪一行。

- source_path可以修改源码路径
-  应该使用命令
`go tool pprof -source_path=$GOPATH/personal/demo_new -trim_path=$GOPATH/personal/demo_old <file>/<url>`

### 命令行模式
```sh
go tool pprof -source_path=/path/  flie/url
```
### web 模式
```sh
go tool pprof -http localhost:8181 -source_path=/Users/matytan/go/src/filename/ profile
```

- 指标

flat： 采样时，该函数正在运行的次数*采样频率(10ms)，即得到估算的函数运行〞采样时间”。这里不包括函数等待子函数返回。

flat%： flat / 总采样时间值

sum%：前面所有行的 flat% 的累加值，如第二行 sum% = 20.82%= 11.12%+ 9.70% cum：采样时，该函数出现在调用堆栈的采样时间，包括函数等待子函数返回。因此 flat <=cum

cum%：cum/ 总采样时间值
![](https://raw.githubusercontent.com/matyle/tupic/master/img/20201101145658109.png)
