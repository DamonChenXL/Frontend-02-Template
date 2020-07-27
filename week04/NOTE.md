#### 浏览器总论 | 浏览器的工作原理总论

#### 状态机 | 有限状态机

- 每一个状态都是一个机器

* 在每一个机器里，我们可以做计算、存储、输出......
* 所有的这些机器接受的输入是一致的
* 状态机的每一个机器本身没有状态，如果我们用函数来表示的话，它应该是纯函数（无副作用）

- 每一个机器知道下一个状态

* 每个机器都有确定的下一个状态 （Moore）
* 每个机器根据输入决定下一个状态 （Mealy）

##### JS 中的有限状态机(Mealy)

`//每个函数是一个状态 function state(input){ //函数参数就是输入 //在函数中，可以自由地编写代码，处理每个状态的逻辑 return next;//返回值作为下一个状态 } //////以下是调用/////// while(input){ //获取输入 state=state(input);//把状态机的返回值作为下一个状态 }`

#### 状态机 | 不使用状态机处理字符串（一）

##### 在一个字符串中，找到字符”a”

`function match(string){ for(let c of string){ if(c==='a'){ return true } } return false; } match("I am groot")`

#### 状态机 | 不使用状态机处理字符串（二）

##### 在一个字符串中，找到字符”ab”

`function match(string){ let foundA=false; for(let c of string){ if(c==="a"){ foundA=true; }else if(foundA && c==="b"){ return true }else{ foundA=false; } return false; } } console.log(match("I acbm groot"));`

#### 状态机 | 不使用状态机处理字符串（三）

##### 在一个字符串中，找到字符”abcdef”

> 代码过于复杂

#### 状态机 | 使用状态机处理字符串（一）

`function match(string){ let state=start; for(let c of string){ state=state(c); } return state===end; } function start(c){ if(c==="a"){ return foundA; }else{ return start(c) } } function end(c){ return end } .... 以此类推 console.log(match("I acbm groot"));`

> 详情代码见 status01.js

#### 状态机 | 使用状态机处理字符串（二）

> 详情代码见 status02.js 必做作业 status03.js

#### HTTP 请求 | HTTP 的协议解析

##### ISO-OSI 七层网络模型

- 应用
- 表示
- 会话
- 传输
- 网络
- 数据链路
- 物理层
  > 4G/5G/Wi-Fi : 数据链路层 物理层 ； Internet:网络； TCP：传输； HTTP: 应用 表示 会话

##### TCP/IP 的一些基础知识

- 流
- 端口
- require("net")
- 包
- IP 地址
- libnet/libpcap

##### HTTP

- Request
- Response

#### HTTP 请求 | 服务端环境准备

- 服务端 server.js

#### HTTP 请求 | 实现一个 HTTP 的请求

- 客户端 client.js

##### 第一步 HTTP 请求总结

- 设计有一个 HTTP 请求的类
- content type 是一个必要的字段，要有默认值
- body 是 kv 格式
- 不同的 content-type 影响 body 的格式

#### HTTP 请求 | send 函数的编写，了解 response 格式

> 具体看 client.js

##### 第二步 send 函数总结

- 在 Request 的构造器中收集必要的信息
- 设计一个 send 函数，把请求真是发送到服务器
- send 函数应该是异步的，所以返回 Promise

#### HTTP 请求 | 发送请求

> 具体看 client.js 补全 send 里面代码

##### 第三步 发送请求

- 设计支持已有的 connection 或者自己新建 connection
- 收到数据传给 parser
- 根据 parser 状态 resolve Promise

#### HTTP 请求 | response 解析

##### 第四步 ResponseParser 总结

- Response 必须分段构造，所以我们要用一个 ResponseParser 来 “装配”
- ResponseParser 分段处理 ResponseText，我们用状态机来分析文本结构

#### HTTP 请求 | response body 的解析

> 具体看 client.js 补全 Responsebody 代码

##### 第五步 BodyParser 总结

- Response 的 body 可能根据 Content-Type 有不同的结构，因此我们会采用 Parser 的结构来解决问题
- 以 TrunkBodyParser 为例，我们同样用状态机来处理 body 的格式

#### HTTP 请求 | HTML parse 模块的文件拆分

> 具体看 client.js

##### 第一步总结

- 为了方便文件管理，我们把 parser 单独拆到文件中
- parser 接受 HTML 文本作为参数，返回一颗 DOM 树

#### HTML 解析 | 用 FSM 实现 HTML 的分析

> 具体看 parser.js

##### 第二步总结

- 我们用 FSM 来实现 HTML 的分析
- 在 HTML 标准中，已经规定了 HTML 的状态
- Toy-Browser 只挑选其中一部分状态，完成一个最简版本

#### HTML 解析 | 解析标签

> 具体看 parser.js

##### 第三步总结

- 主要的标签有: 开始标签，结束标签和自封闭标签
- 在这一步我们暂时忽略属性

#### HTML 解析 | 创建元素

> 具体看 parser.js

##### 第四步总结

- 在状态机中，除了状态迁移，我们还会要加入业务逻辑
- 我们在标签结束状态提交标签 token

#### HTML 解析 | 处理属性

> 具体看 parser.js

##### 第五步总结

- 属性值分为单引号、双引号、无引号三种写法，因此需要较多状态处理
- 处理属性的方式跟标签类似
- 属性结束时，我们把属性加到标签 Token 上

#### HTML 解析 | 用 token 构建 dom 树

> 具体看 parser.js

##### 第六步总结

- 从标签构建 DOM 树的基本技巧是使用栈
- 遇到开始标签是创建元素并入栈，遇到结束标签时出栈
- 自封闭节点可视为入栈后立刻出栈

#### HTML 解析 | 将文本节点加到 DOM 树

> 具体看 parser.js

##### 第七步总结

- 文本节点与自封闭标签处理类似
- 多个文本节点需要合并
