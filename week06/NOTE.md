#### CSS 总论| CSS 语法的研究

- @charset
- @import
- rules

* @media
* @page
* rule

#### CSS 总论|CSS @规则的研究

##### At-rules

- [@charset](https://www.w3.org/TR/css-syntax-3/)
- [@import](https://www.w3.org/TR/css-cascade-4/)
- [@media](https://www.w3.org/TR/css3-conditional/)
- [@page](https://www.w3.org/TR/css-page-3/)
- [@counter-style](https://www.w3.org/TR/css-counter-styles-3)
- [@keyframes](https://www.w3.org/TR/css-animations-1/)
- [@fontface](https://www.w3.org/TR/css-fonts-3/)
- [@supports](https://www.w3.org/TR/css3-conditional/)
- [@namespace](https://www.w3.org/TR/css-namespaces-3/)

#### CSS 总论|CSS 规则的结构

##### CSS 规则

- 选择器
- 声明（Key,Value）

- Selector
  [https://www.w3.org/TR/selectors-3/](https://www.w3.org/TR/selectors-3/)
  [https://www.w3.org/TR/selectors-4/](https://www.w3.org/TR/selectors-4/)
- Key
  Properties
  [Variables](https://www.w3.org/TR/css-variables/)
- Value
  [https://www.w3.org/TR/css-values-4/](https://www.w3.org/TR/css-values-4/)

#### CSS 总论| 收集标准

#### CSS 总论| CSS 总论总结

- CSS 语法
- at-rule
- selector
- variables
- value
- 实验

#### CSS 选择器 | 选择器语法

##### 简单选择器

- \*
- div svg|a
- cls
- #id
- \[attr=value]
- :hover
- ::before

##### 复合选择器

- <简单选择器><简单选择器><简单选择器>
- \*或者 div 必须写在最前面

##### 复杂选择器

- <复合选择器><sp><复合选择器>
- <复合选择器>">"<复合选择器>
- <复合选择器>"~"<复合选择器>
- <复合选择器>"+"<复合选择器>
- <复合选择器>"||"<复合选择器>

#### CSS 选择器 | 选择器的优先级

#### CSS 选择器|伪类

##### 链接/行为

- :any-link
- :link :visited
- :hover
- :active
- :focus
- :target

##### 树结构

- :empty
- :nth-child()
- :nth-last-child()
- :first-child :last-child :only-child

##### 逻辑型

- :not 伪类
- :where :has

#### CSS 选择器 | 伪元素

- ::before
- ::after
- ::first-line
- ::first-letter
