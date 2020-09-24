#### CSS 排版 | 盒

> HTML 代码中可以书写开始标签，结束标签，和自封闭标签。
> 一对起止标签，表示一个元素
> DOM 树中储存的是元素和其他类型的节点（Node）
> CSS 选择器选中的是元素
> CSS 选择器选中的是元素，在排版时可能产生多个盒
> 排版和渲染的基本单位是盒

##### 盒模型 boxing-sizing

- content-box (content=width)
- border-box (border+padding+content=width
  )

#### CSS 排版 | 正常流

##### 正常流排版

- 收集盒进行
- 计算盒在行中的排布
- 计算行的排布

> BFC: 从上往下排布的上下文 IFC:从左到右排列的上下文

#### CSS 排版 | 正常流的行级排布

##### vertical-align

- text-bottom
- text-top
- baseline
- line-top
- line-bottom

#### CSS 排版 | 正常流的块级排布

##### float 与 clear

##### 只有BFC正常流才会产生 margin collapse