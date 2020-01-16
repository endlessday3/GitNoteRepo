# An Overview of Go’s Tooling - Alex Edwards
## 工具的安装
- 当不在go module目录下使用`go get`下载安装模块时,由于`GO111MODULE`默认不为on即默认为auto自动识别，所以为了能享受到`GOPROXY`带来的下载速度，安装时需临时设置`GO111MODULE`环境变量，完整命令如下
- `GO111MODULE=on go get golang.org/x/tools/cmd/stress`

## Go的一些环境变量
- go env
- go help environment

## 


