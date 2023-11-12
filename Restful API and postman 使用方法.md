#  Restful API and postman 使用方法

## RESTful API


REST API（也称为 RESTful API）是一种符合 REST 架构风格约束并允许与 RESTful Web 服务交互的应用程序编程接口（API 或 Web API）。 REST (representational state transfer)代表代表性状态转移，由计算机科学家 Roy Fielding 创建

## API

API 是一组用于架构和集成应用程序软件的定义和协议。它有时被称为信息提供者和信息用户之间的契约—建立消费者所需的内容（调用）和生产者所需的内容（响应。换句话说，如果你想要与计算机或系统交互以检索信息或执行功能，API 可以帮助您向该系统传达您想要的内容，以便它能够理解并满足请求。

您可以将 API 视为消费端或服务端端与他们想要获取的资源或 Web 服务之间的中介。这也是组织共享资源和信息，同时维护安全性、控制和身份验证的一种方式——确定谁可以访问什么。

API 的另一个优点是您不必了解缓存的细节 - 如何检索资源或资源来自何处。

## REST

REST 是一组架构约束，而不是协议或标准。 API 开发人员可以通过多种方式实施 REST。

当通过 RESTful API 发出客户端请求时，它将资源状态的表示形式传输给请求者或端点。此信息或表示形式通过 HTTP 以多种格式之一传递：JSON（Javascript 对象表示法）、HTML、XLT、Python、PHP 或纯文本。 JSON 是最常用的文件格式，因为尽管它的名称如此，但它与语言无关，并且人类和机器都可读。

其他需要记住的事情：标头和参数在 RESTful API HTTP 请求的 HTTP 方法中也很重要，因为它们包含重要的标识符信息，例如请求的元数据、授权、统一资源标识符 (URI)、缓存、cookie 和更多的。有请求标头和响应标头，每个标头都有自己的 HTTP 连接信息和状态代码。



##  Restful API 需要遵循的标准

1. 客户端-服务器架构由客户端、服务器和资源组成，并且通过 HTTP 管理请求
2. [无状态](https://www.redhat.com/zh/topics/cloud-native-apps/stateful-vs-stateless)客户端-服务器通信，即 get 请求间隔期间，不会存储任何客户端信息，并且每个请求都是独立的，互不关联
3. 可缓存性数据：可简化客户端-服务器交互。
4. 组件间的统一接口：使信息以标准形式传输。这要求：
   1. 所请求的资源可识别并与发送给客户端的表述分离开。
   2. 客户端可通过接收的表述操作资源，因为表述包含操作所需的充足信息。
   3. 返回给客户端的自描述消息包含充足的信息，能够指明客户端应该如何处理所收到的信息。
   4. 超文本/超媒体可用，是指在访问资源后，客户端应能够使用超链接查找其当前可采取的所有其他操作。
5. 组织各种类型服务器（负责安全性、负载平衡等的服务器）的分层系统会参与将请求的信息检索到对客户端不可见的层次结构中。
6. 按需编码（可选）：能够根据请求将可执行代码从服务器发送到客户端，从而扩展客户端功能。



##  postman

postman是一块功能强大的页面调试和发送页面http请求（常用），新版本的postman 除了发送http请求 以外，可以发送 

![image-20231108000258235](/Users/Albert_1/huawei/tranning_doc/imgs/:Users:Albert_1:huawei:tranning_doc:imgs:Users:Albert_1:Library:Application Support:typora-user-images:image-20231108000258235.png)

### 操作介绍

![洁面](https://s5.51cto.com/oss/202207/15/56b59186578b0138b7818318e90c11e32d93f0.jpg)

### postman sidebar介绍

![image-20231108230612207](/Users/Albert_1/Library/Application Support/typora-user-images/image-20231108230612207.png)



1. collections 用来创建文件夹，分类存储创建的请求 （常用）
2. apis  用来倒入和创建apis接口定义，常用的问swager3.0 的语法（类似我们在开发接口时候定义的api）
3. environments 用来管理自定义的请求环境 可以是可创建全局变量，局部变量 （常用）
4. history 查询你调用过的api 请求 （常用）

##  collections

postman 的collections 是用来存储 和管理请求，使用collections 我们可以更好给请求进行分组和管理，并且可以用来依靠collections做一些骚操作

1. 导出，倒入，分享，fork
2. 自动化测试
3. 执行测试



## postman主要操作



### 发送请求

postman 最常用的功能就是发送求情



> 发送 www-form-urlencoded请求



![](https://s8.51cto.com/oss/202207/15/64e1dd4301aff74ae2b2237a4b5218b8b34356.jpg)



> 发送文件



![](https://s5.51cto.com/oss/202207/15/047ec0f128083a8e1eb02966be88cfa2eeb7ce.jpg)

> 发送json

![](https://s6.51cto.com/oss/202207/15/89cec76915455a88c7e621e4c971c1ddaabf1b.jpg)

### 查看请求

响应数据是发送请求后经过服务器处理后返回的结果，响应由三部分组成，分别是状态行、响应头、响应体。我们来看下postman的响应数据展示。

![](https://s5.51cto.com/oss/202207/15/687d7c704cf0d67e5812180d95baf591d5375f.jpg)



### 查看执行日志

![img](https://s2.51cto.com/oss/202207/15/19321aa640fee1732806733fc4ae7f7dca7541.jpg)

![img](https://s5.51cto.com/oss/202207/15/629cea068caeea55ac9798ee6459fd74426586.jpg)



### 断言

如果没有断言，我们只能做接口的功能测试，但有了断言后，就为我们做自动化提供了条件，并且在postman中的断言是非常方便和强大的 。

在tests这边可以设置检查语句

![img](https://s8.51cto.com/oss/202207/15/c352b5466ab1f2c3b78351e6214221a91927bb.jpg)

常用的断言语句

> 200 检查

```javascript
pm.test("Status code is 200", function () {
   pm.response.to.have.status(200); //这里填写的200是预期结果，实际结果是请求返回结果
});
```



> 检查response header



```javascript
pm.test("Content-Type is present", function () {
   pm.response.to.have.header("Content-Type"); //断言响应头存在"Content-Type"
});
```



###  环境变量

变量可以使我们在请求或脚本中存储和重复使用其值，通过将值保存在变量中，可以在集合，环境或请求中引用。

对我们做接口测试来说，又是一个非常重要的功能 。

在postman常用的三种变量分别是全局变量，环境变量，集合变量 。

1. 全局变量： 作用域最大
2. 环境变量： 可以切换使用，可以设置多个只
3. collections 变量，集合使用

> 在请求中使用变量



![img](https://s9.51cto.com/oss/202207/15/c27c55f727446325936611c27842eb2429b408.jpg)



###  导入请求



![image-20231112225735185](/Users/Albert_1/huawei/tranning_doc/imgs/:Users:Albert_1:Library:Application Support:typora-user-images:image-20231112225735185.png)

###  

### 显示代码

postman可以将请求转换成 许多语言的代码，如python java go curl等

![image-20231112230759445](/Users/Albert_1/huawei/tranning_doc/imgs/:Users:Albert_1:Library:Application Support:typora-user-images:image-20231112230759445.png)



##  参考资料

1. [https://restfulapi.net/rest-architectural-constraints/](https://restfulapi.net/rest-architectural-constraints/)
1. [https://www.redhat.com/zh/topics/api/what-is-a-rest-api](https://www.redhat.com/zh/topics/api/what-is-a-rest-api)