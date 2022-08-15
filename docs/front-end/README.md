# 前端

记录前端知识。

前端三件套：HTML、CSS、JavaScript

* HTML决定了页面的显示内容；

* CSS决定了美观程度；

* JavaScript修饰页面特效



## HTML（**H**yper **T**ext **M**arkup **L**anguage）

超文本标记语言，是解释型语言，不是编译型

### 基本标签

* html页面中由一对标签组成：`<html></html>`
  * `<html>` 称之为 开始标签
  * `</html>`称之为 结束标签
* title： 表示网页的标题
* meta：可以在meta标签中设置编码方式`<meta charset = "utf-8">`
* br：`<br/>`表示换行 。br标签是一个单标签。
  * 单标签：开始标签和结束标签是同一个，斜杠放在单词后面
* p：表示段落标签
* img：标签图片标签
  * src属性表示图片文件的路径
  * width和height表示图片的大小
  * alt表示图片的提示
* h1~h6：标题标签
* 列表标签：
  * ol 有序列表，start属性表示从*开始，type属性表示显示的类型：A a I i 1(deafult)
  * ul 无序列表，type disc(default) , circle , square
* u 下划线（underline） b 粗体（bold）  i 斜体（italics）
* 上标 sup  下标 sub
* 特殊符号：小于号 &lt; `&lt;` 大于等于号 &ge; `&ge;` 版权 &copy; `&copy;`
* span 不换行的块标记
* a 表示超链接
  * href 链接的地址
  * target：
    * _self 在本窗口打开
    * _blank 在一个新窗口打开
    * _parent 在父窗口打开
    * _top  在顶层窗口打开
* div 层

### table标签

* 表格  table
* 行    tr
* 列    td
* 表头列   th
* table中有如下属性（虽然已经淘汰，但是最好了解一下）
  * border：表格边框的粗细
  * width:表格的宽度
  * cellspacing：单元格间距
  * cellpadding：单元格填充
* tr中有一个属性： align -> center , left , right 
* 合并
  * rowspan : 行合并
  * colspan : 列合并

### 表单标签

* 表单 form
  * action  提交后触发的方法
  * method  一般选择post
* 表单中的标签（其中 name属性必须要指定，否则这个文本框的数据将来是不会发送给服务器的）
  * input type="text" 表示文本框 ， 
  * input type="password" 表示密码框
  * input type="radio" 表示单选按钮。需要注意的是，name属性值保持一致，这样才会有互斥的效果；可以通过checked属性设置默认选中的项
  * input type="checkbox" 表示复选框。name属性值建议保持一致，这样将来我们服务器端获取值的时候获取的是一个数组
  * select 表示下拉列表。每一个选项是option，其中value属性是发送给服务器的值 , selected表示默认选中的项
  * textarea 表示多行文本框（或者称之为文本域）,它的value值就是开始结束标签之间的内容
  * input type="submit" 表示提交按钮
  * input type="reset" 表示重置按钮
  * input type="button" 表示普通按钮

### 其他

* frameset 表示页面框架 （这个标签已经淘汰，了解，不需要掌握）

  * frame表示框架中的具体页面引用

  * iframe 在一个页面嵌入一个子页面

  * 示例：

    * ```html
      <html>
      	<head></head>
      	<frameset rows="20%,*" > <!-- frameborder="no" -->
      		<frame src="frames/top.html"/>
      		<frameset cols="15%,*">
      			<frame src="frames/left.html"/>
      			<frameset rows="80%,*">
      				<frame src="frames/main.html"/>
      				<frame src="frames/bottom.html"/>
      			</frameset>
      		</frameset>
      	</frameset>
      </html>
      ```





## CSS（**C**ascading **S**tyle **S**heets）

层叠式样式表



## JavaScript



