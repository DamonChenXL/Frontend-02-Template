#### 重学 HTML | HTML 的定义：XML 与 SGML

#### 重学 HTML | HTML 标签语义

#### 重学 HTML | HTML 语法

##### 合法元素

- Elemnt:<tagname>...</tagname>
- Text:text
- Comment:<!--comments-->
- DocumentType:<!Doctype html>
- ProcessingInstruction:<?a 1?>
- CDATA:<![CDATA[]]>

##### 字符引用

- &#161;
- &amp;
- &lt;
- &quot;

#### 浏览器 API | DOM API

##### 导航类操作

- parentNode
- childNodes
- firstChild
- lastChild
- nextSibling
- prviousSibling
- parentElement
- children
- firstElementChild
- nextElmentSibling
- previousElementSibling

##### 修改操作

- appendChild
- insertBefore
- removeChild
- replaceChild

##### 高级操作

- compareDocumentPosition 是一个用于比较两个节点中关系的函数。
- contains 检查一个节点是否包含另一个节点的函数
- isEqualNode 检查两个节点是否完全相同。
- isSameNode 姜茶两个节点是否是同一个节点，实际上在 JavaScript 中可以用“===”。
- cloneNode 复制一个节点，如果传入参数 true，则会连同子元素做深拷贝。

#### 浏览器 API | 事件 API

##### Event: 冒泡与捕获

#### 浏览器 API | Range API

##### Range API（1）

- var range = new Range()
- range.setStart(element,9)
- range.setEnd(element,4)
- var range = document.getSelection().getRangeAt(0);

##### Range API（2）

- range.setStartBefore
- range.setEndBefore
- range.setStartAfter
- range.setEndAfter
- range.selectNode
- range.selectNodeContant

##### Range API（3）

- var fragment=range.extractContents()
- range.insertNode(document.createTextNode("aaaa"));

#### 浏览器 API | CSSOM

##### Rules

- document.styleSheets[0].cssRules
- document.styleSheets[0].insertRule("p {color:pink;}",0)
- document.styleSheets[0].removeRule(0)

##### Rule

- CSSStyleRule

* selectorText String
* style K-V 结构

##### getComputedStyle

- window.getComputedStyle(elt,pseudoElt);
  (elt 想要获取的元素，pseudoElt 可选，伪元素)

#### 浏览器 API | CSSOM View

##### window

- window.innerHeight,window.innerWidth
- window.outerWidth,window.outerHeight
- window.devicePixelRatio
- window.screen(window.screen.width,window.screen.height,window.screen.availWidth,window.screen,availHeight)

##### window API

- window.open("about:blank","\_blank","width=100,height=100,left=100,right=100")
- moveTo(x,y)
- moveBy(x,y)
- resizeTo(x,y)
- resizeBy(x,y)

##### scroll
- scrollTop
- scrollLeft
- scrollWidth
- scrollHeight
- scroll(x,y)
- scrollBy(x,y)
- scrollIntoView()

##### window
- scrollX
- scrollY
- scroll(x,y)
- scrollBy(x,y)

##### layout
- getClientRects()
- getBoundingClientRect()

#### 浏览器API | 其他API

- khronos(WebGL)
- ECMA(ECMAScript)
- WHATWG(HTML)
- W3C(webaudio、CG/WG)
