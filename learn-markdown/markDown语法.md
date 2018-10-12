#标题
>两种格式的标题：
>1.Setext格式：“\<h1>\<h2>”或者由等号“=”和“-”的下划线创建；
>标题示例
>====
>小标题示例
>-----
>2.Atx格式："#"在行的开头放置1-6个哈希标记，哈希数等于生成的html标题级别。

#换行
如要强制换行，需要在行结尾加上两个空格符和回车符。

* this two-line bullet   
	won't break

#块引用 - blockquote
>块引用使用">"尖括号表示。

#使用"\*"和下划线表示重点

>这里是一级*重点* //斜体
>这里是二级**重点** //加粗
>这里是三级***重点*** //加粗+斜体

#无序列表 - List
>无序（项目符号）列表使用**星号，加号和连字符（\*， \+，和 \-）+ tab** 作为列表标记。这三个标记是可互换的。

>1.	**\*** 星号
>	*	Candy.
>	* 	Gum.
>	* 	Booze.
>2.	**\+** 加号
>	+	Candy.
>	+	Gum.
>	+	Booze.
>3. **\-** 减号
>	-	Candy.
>	- 	Gum.
>	- 	Booze.

#有序列表 - orderList
> 1.	red
>	*	玫瑰红
>	* 	草莓红
> 2.	blue
> 3. yellow

#链接
>两种方式创建链接：*内敛* 和*引用*，可以使用方括号来分隔要转换为链接的文本

>*	**内联样式：链接在链接文本后立即使用括号**

>	点击进入[百度](https:baidu.com "with a title")
	
>* 	**引用样式：允许您按名称引用链接，您可以在文档的其他位置定义它们：**

>	I get 10 times more traffic from [Google][1] than from
[Yahoo][2] or [MSN][3].

[1]: http://google.com/        "Google"
[2]: http://search.yahoo.com/  "Yahoo Search"
[3]: http://search.msn.com/    "MSN Search"
	
>	I start my morning with a cup of coffee and
[The New York Times][NY Times].

[ny times]: http://www.nytimes.com/

#图片
>图片类似于连接，也是**内敛**和**引用**两种方式
>
>*	**内敛**
>
	![alt text](/Users/evan-ac/Downloads/柯南.jpg "Title")
>* **引用** 
>
>	![alt text][id]

[id]: /Users/evan-ac/Downloads/柯南.jpg "Title"
	
#代码块
>在常规段落中，您可以通过在`反引号`包装文本来创建代码范围。任何＆符号（&）和尖括号（<或 >）都将自动转换为HTML实体。这使得使用Markdown轻松编写HTML示例代码：

I strongly recommend against using any `<blink>` tags.
I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.

>要指定整个预格式化代码块，请将块的每一行缩进4个空格或1个制表符。就像使用代码跨越，&，<，和>字符将被自动转义。
If you want your page to validate under XHTML 1.0 Strict,
you've got to put paragraph tags in your blockquotes:

	int a = 0;
	inb b = 0;
	function sum(int a,int b) {
		return a+b;
	}
	int c = sum(a,b);
	
> 或者直接通过以下方式：

```objc
int a = 0;
inb b = 0;
- (int)sumWithA:(int)a andB:(int) b {
	return a+b;
}
int c = [self sumWithA:10 andB:20];
 
 ```
#分行
如果你打三个星号 `***` 或者三个下划线 `---` 在一行中，我会展示分行。
