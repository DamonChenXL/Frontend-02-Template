#### 语言按语法分类

##### 非形式语言：中文 英文；
##### 形式语言（乔姆斯基谱系）： 
1.0型-无限制文法  
2.1型-上下文相关文法 
3.2型-上下文无关文法 
4.3型 正则文法

#### 产生式（BNF）
+ 用尖括号括起来的名称来表示语法结构名
+ 语法结构分成基础结构和需要用其他语法结构定义的复合结构
  * 基础结构称终结符
  * 复合结构称非终结符
+ 引号和中间的字符表示终结符
+ 可以有括号
+ *表示重复多次
+ |表示或
+ 表示至少一次
>这块理解太深 感觉是编译原理这块知识 

#### 通过产生式理解乔姆斯基谱系
+ 0型 无限制文法
  ` ?::=?`
+ 1型 上下文相关文法
 ` ?<A>?::=?<B>?`
+ 2型 上下文无关文法
    `<A>::=?`
+ 3型 正则文法
    `<A>::=<A>?  <A>::=?<A> X`


#### 语言的分类
+ 形式语言 - 用途 （数据描述语言 编程语言）
+ 表达式 - 声明式语言 命令式语言

#### 图灵完备性
+ 图灵完备性： 命令式 --- 图灵机 
 * goto
 * if和while
+ 声明式 ---lambda
 * 递归

#### 一般命令式编程语言
##### Atom
+ Identifier
+ Literal
##### Expression
+ Atom
+ Operator
+ Punctuator
##### Statement
+ Expression
+ Keyword
+ Punctuator
##### Structure
+ Function
+ Class
+ Process
+ Namespace
+ ...
##### Program
+ Program
+ Module
+ Package
+ Library

#### JS类型 - Number (IFFF)
> Null 有值代表空 Underfined代表根本没人定义过它的值
 双精度浮点数 1 - 正负 11个指数 53个底数

#### JS类型 - String
> ASCII -> Unicode -> UCS ->GB (GB2312 -> GBK -> GB18030) -> ISO-8859 -> BIG 5
>"abc" 'abc' `abc`
> 转移符号 bfnrtv
#### JS类型 - 其他类型
##### Types 
+ Number
+ String 
+ Boolean
+ Object
+ Null
+ Undefined
+ Symbol

#### Object API/Grammar
+ {} .[] Object.defineProperty
+ Object.create/ Object.setPrototypeOf /Object.getPrototypeOf
+ new / class /extends
+ new / function / prototype