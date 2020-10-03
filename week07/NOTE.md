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

##### 只有 BFC 正常流才会产生 margin collapse

#### CSS 排版 | BFC 合并

##### Block

- Block Container:里面有 BFC 的（能容纳正常流的盒，里面就有 BFC，想想有哪些）
- Block-level Box:外面有 BFC 的
- Block Box =Block Container +Block-level Box:里外都有 BFC

##### Block Container

- block
- inline-block
- table-cell
- flex-item
- grid cell
- table-caption

##### Block-level Box

###### Block level

- display:block
- display:flex
- display:table
- display:grid
- ......

###### Inline level

- display:inline-block
- display:inline-flex
- display:inline-table
- display:inline-grid
- ......

#### CSS 排版 | Flex 排版

##### Flex 排版

- 收集盒进行
- 计算盒在主轴方向的排布
- 计算盒在交叉轴方向的排布

#### CSS 动画与绘制 | 动画

##### Animation

- @keyframes 定义
- animation:使用

##### Animation 属性

- animation-name 时间曲线
- animation-duration 动画的时长
- animation-timing-function 动画的时间曲线
- animation-delay 动画开始前的延迟
- animation-iteration-count 动画的播放次数
- animation-direction 动画的方向

##### Transition 属性

- transition-property 要变换的属性
- transtion-duration 变换的时长
- transition-timing-function 时间曲线
- transition-delay 延迟

#### CSS 动画与绘制 | 颜色

##### CMYK 与 RGB

##### HSL 与 HSV

#### CSSS 动画与绘制 | 绘制

##### 几何图形

- border
- box-shadow
- border-radius

##### 文字

- font
- text-decoration

##### 位图

- background-image
