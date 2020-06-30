# API文档
本文档用于老师检查，由于本项目客户端和服务端都在用户主机上，本项目不存在接口只存在函数调用。但由于实训方要求，所以仍然编写了这个接口(~~函数~~)文档。

### openConnection
简要描述
+	用户打开与p2p节点的连接，涉及节点注册与节点发现，即节点初始化。

请求URL
+	openConnection

请求方式
+	函数调用

参数
+ 无 

返回值
+ 成功则打开连接
+ 失败返回error

### sendMsg
简要描述
+	用户通过之前建立的连接发送消息

请求URL
+	sendMsg

请求方式
+	函数调用

参数
```
Message{
    msgType:,
    msgData:,
    } 
```
返回值
+ 成功则返回success
+ 失败返回error

### getMsg
简要描述
+	用户监听之前建立的连接中的消息

请求URL
+	getMsg

请求方式
+	监听

参数
+  无

返回值
+ 成功则返回Message
+ 失败返回error