#### JS 表达式 | 运算符和表达式

##### Member 运算

- a.b
- a[b]
- foo`string`
- super.b
- super['b']
- new.target
- new Foo()

##### Reference(引用)

- Object
- key

##### Call Expressions

###### Call

- foo()
- super()
- foo()['b']
- foo().b
- foo()`abc`

> Member 优先级大于 call

##### left handside & right handside

- a.b=c
- a+b=c

##### Update Expressions

###### Update

- a++
- a--
- --a
- ++a

##### Unary Expressions

- delete a.b
- void foo()
- typeof a
- +a
- -a
- ~a
- !a
- await a

##### Exponental Expressions 右结合运算 从右边开始算

> \*\* 乘方运算

##### Expressions

- Multiplicative
  > - / %
- Additive
  > - -
- Shift
  > << >> >>>
- Relationship
  > < > <= >= instanceof in
- Equality
  > == != === !==
- Bitwise
  > & ^ |
- Logical
  > && ||
- Conditional
  > ?:

#### JS 表达式 | 类型转换

##### Type Convertion

| \*\*\*\*  |     Number     |           String | Boolean  | Undefined | Null | Object | Symbol |
| --------- | :------------: | ---------------: | :------: | --------: | :--: | -----: | ------ |
| Number    |       -        |                  | 0 false  |         x |  x   | Boxing | x      |
| String    |                |                - | "" false |         x |  x   | Boxing | x      |
| Boolean   | true 1 false 0 |    'true''false' |    -     |         x |  x   | Boxing | x      |
| Undefined |      NaN       |      'Undefined' |  false   |         - |  x   |      x | x      |
| Null      |       0        |           'null' |  false   |         x |  -   |      x | x      |
| Object    |    valueOf     | valueOf toString |   true   |         x |  x   |      - | x      |
| Symbol    |       x        |                x |    x     |         x |  x   | Boxing | -      |

##### Unboxing 拆箱转换

- ToPremitive
- toString vs valueOf
- Symbol.toPrimitive

##### boxing 装箱转换

| 类型    | 对象                    | 值          |
| ------- | ----------------------- | ----------- |
| Number  | new Number(1)           | 1           |
| String  | new String("a")         | "a"         |
| Boolean | new Boolean(true)       | true        |
| Symbol  | new Object(Symbol("a")) | Symbol("a") |

#### JS 语句 | 运行时相关概念

##### Statement

###### Grammar

- 简单语句
- 组合语句
- 声明

###### Runtime

- Completion Record
- Lexical Environment

##### Completion Record

- [[type]] normal.break,continue,return,or throw
- [[value]] 基本类型
- [[target]] label

#### JS 语句 | 简单语句和复合语句

##### 简单语句

- ExpressionStatement(最核心)
- EmptyStatement
- DebuggerStatement
- ThrowStatement
- ContinueStatement
- BreakStatement
- ReturnStatement

##### 复合语句

- BlockStatement
  > {
      ...
      ...
      ...
  }
- IfStatement
- SwitchStatement
- IterationStatement (循环)
  > while、 do while、 for 循环、 for in 循环 、for of 循环、
- WithStatement
- LabelledStatement
- TryStatement

#### 声明

- FunctionDeclaration
- GeneratorDeclaration
- AsyncFunctionDeclaration
- AsyncGeneratorDeclaration
- VariableStatement
- ClassDeclaration
- LexicalDeclaration

##### 声明

- function
- function\*
- async function
- async function\*
- class
- const
- let

##### 预处理

`var a=2; void function(){ a=1; return; var a; }(); console.log(a);`

#### 作用域

#### JS 结构化 | 宏任务和微任务

##### JS 执行粒度 （运行时）

- 宏任务
- 微任务（Promise）
- 函数调用 （Execution Context）
- 语句/声明（Completion Record）
- 表达式 （Reference）
- 直接量/变量/this ......

#### JS 结构化 | JS 函数调用

##### Execution Context

- code evaluation state
- Function
- Realm
- LexicalEnvironment

* this
* new.target
* super
* 变量

- Script or Module
- VariableEnvironment
- Generator
