### cobra 使用说明

#### 初始化项目
cobra init [app] 会在go path目录中创建相应的app应用，如果go path中存在对应的app，则失败

	cobra支持全路径（相对于go path来说的目录）

#### 添加命令
如果你的应用包含多个区块的功能

比如

* app serve
* app config
* app config create 这个是config的子命令


在项目的目录中（main.go)所在的目录，执行以下命令

```
cobra add serve
cobra add config
cobra add create -p 'configCmd' # 把config作为一个命令

```
需要注意的是，不要使用蛇形写法来声明cmd

然后

At this point you can run `go run main.go` and it would run your app. `go run main.go serve`, `go run main.go config`, `go run main.go config create` along with `go run main.go help serve`, etc. would all work.

