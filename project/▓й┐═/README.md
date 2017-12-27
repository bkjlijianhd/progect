
#### 准备条件
安装最新版[Node.js](https://nodejs.org/en/download/)、[bower](http://bower.io/)、[MongoDB](https://www.mongodb.org/downloads/)、[Redis](http://redis.io/download/)。  
（注：如果使用Windows平台，可以去[https://github.com/MSOpenTech/redis/releases](https://github.com/MSOpenTech/redis/releases)下载安装Redis）
#### 安装依赖
* 服务端依赖  
```Shell
$ npm install
```
* 客户端依赖  
```Shell
$ bower install
```

#### 参数配置
根据实际情况修改 config.json 配置文件，DbPath 是MongoDB路径，RedisHost 是Redis所在ip，RedisPort 是Redis端口号。  
```JSON
{
  "DbPath": "mongodb://localhost/iBlog2",
  "RedisHost": "127.0.0.1",
  "RedisPort": 6379
}
```
后台管理员账号信息在 config/account.json 中配置，默认管理员账号 admin ，密码 123456 ，密码需[md5加密](http://md5jiami.51240.com/)存储。
```JSON
{
  "Id": "1",
  "UserName": "admin",
  "Password": "e10adc3949ba59abbe56e057f20f883e"
}
```
在 "后台管理-系统设置" 页面中，支持以可视化方式配置其余参数。
#### 启动站点  
*注意：对于node v4及以下版本，需要添加 --harmony-proxies 参数。*  

* 方式1：普通模式启动
```Shell
$ node ./bin/www 
```
* 方式2：快速启动
```Shell
$ npm start
```
* 方式3：守护进程启动  
_守护进程能够发挥多核CPU性能，并在出现异常退出后延迟30秒自动重启工作进程。_
```Shell
$ node daemon.js
```
打开浏览器，访问 [http://localhost:3000/](http://localhost:3000)
#### Enjoy it! :smile:
