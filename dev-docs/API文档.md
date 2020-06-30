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


### server
简要描述
+ 接收来自p2p通信子进程的消息并发送给渲染层

请求方式
+ 与端口建立websocket连接


### upperServer
简要描述
+ 获得来自渲染层的信息并传递给p2p通信子进程

请求URL
+ upperMsg

请求方式
+ 监听

参数
```
{
    type:,
    topic:
}
```
返回值
+ 无

### on-nameclose
简要描述
+	通过参数得到RenameDiv组件中的改名信息

请求URL
+	on-nameclose

请求方式
+	通过组件的事件绑定，即@onname-close='父函数名'

参数
+  name

返回值
+ 无

### view
简要描述
+	通过参数得到当前的点击的chatItem组件所代表的channel名字

请求URL
+	view

请求方式
+	通过组件的事件绑定，即@view='父函数名'

参数
+  name

返回值
+ 无

### send
简要描述
+   用户通过点击发送或按下回车触发此函数来发送消息

请求URL
+	send

请求方式
+	通过组件的事件绑定@onclick='send'与@keyup.enter.native="send"调用

参数
+  name
```
sendMsg {
    msgName:''      //发送者昵称
    msgData:''      //消息主体部分
    channelName: '' //当前所在频道名称
}
 ```

返回值
+ 无

### newMsg
简要描述
+   聊天界面通过此函数接收消息

请求URL
+	newMsg

请求方式
+	父组件通过子组件的引用进行调用

参数
+  name
```
msg {
    msgName:''      //发送者昵称
    msgData:''      //消息主体部分
}
 ```

返回值
+ 无
