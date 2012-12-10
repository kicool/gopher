#Gopher

Golang中国([www.golang.tc](http://www.golang.tc))源代码.

##Requirements

- Go1.0+
- MongoDB
- [github.com/gorilla/mux](http://www.gorillatoolkit.org/)
- github.com/gorilla/sessions
- labix.org/v2/mgo
- bzr(required by mgo)

##Install

    go get github.com/gorilla/mux
    go get github.com/gorilla/sessions
    go get labix.org/v2/mgo
    git clone git://github.com/kicool/gopher.git
	
修改文件 *config.json.default* 为 *config.json* 作为配置文件

- superusers: 内容为用户名,如果没有管理员,内容为"",如果有多个,用空格隔开

内容如下:

    {
        "host": "http://localhost:8888",
        "port": "8888",
        "db": "localhost:27017",
        "cookie_secret": "05e0ba2eca9411e18155109add4b8aac",
        "smtp_username": "username@example.com",
        "smtp_password": "password",
        "smtp_host": "smtp.example.com",
        "smtp_addr": "smtp.example.com:25",
        "from_email": "who@example.com",
        "superusers": "admin,another"
    }

先启动MongoDB

然后运行命令

	go run *.go

或者

    go build -o gopher *.go
    ./gopher

##Contributors

- [Contributors](https://github.com/jimmykuu/gopher/graphs/contributors)


##License

Copyright (c) 2012

Released under the MIT license:

- [www.opensource.org/licenses/MIT](http://www.opensource.org/licenses/MIT)

