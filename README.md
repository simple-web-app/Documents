# Blog
本次的简单 web 服务与客户端开发实战，我们小组选择进行一个简单博客的制作。

分工：

- 前端：[18342090 王超]()
- 后端：[18342067 鲁睿]()、[18342077 南樟](./md/18342077.md)

API：

- Sign in
- Get Articles
- Get Article By Id
- Delete Article
- Get Comments
- Create Comment

API文档：

- [点击这里](./index.html)

### :zap:Quick Start

对于后端部分，使用以下命令进行安装

```
go get https://github.com/simple-web-app/Server/tree/main/go
```

然后在相应文件中进行import

```
import(
	sw "github.com/simple-web-app/Server/tree/main/go"
)
```

在main.go的main函数中添加以下代码即可运行

```
	sw.CreateUser()
	sw.CreateTable()
	sw.CreateComments()
	router := sw.NewRouter()

	log.Fatal(http.ListenAndServe(":8080", router))
```