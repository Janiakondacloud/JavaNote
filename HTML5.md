



# HTML5

![image-20201125195013512](img/image-20201125195013512.png)



## 1.概况

**Hyper Text Markup Language(超文本标记语言)**

**超文本：文字、图片、视频、声音、动画等。。。**

**HTML5的优势：世界知名浏览器厂商对HTML5的支持、市场的需求、跨平台。**

**W3C(WOLRD WIDE WEB CONSORTIUM)万维网联盟指定的标准包括：**

* 结构化标准语言（HTML、XML）
* 表现标准语言（CSS）
* 行为标准（DOM、ECMAScript（JavaScript））

## 2.基本标签

* `<br/>`  换行
* `<strong/>`  加粗
* `<em/>`  斜体
* `<hr/>`  切割
* `&nbsp`  空格
* `&gt`  大于
* `&lt`  小于
* `&copy`  版权

## 3.图像标签

* JPG
* GIF
* PNG
* BMP
* ......

<font color = red>一般单独建立一个文件夹来放静态资源.</font>

```html
 <img src="../img/011.jpg" alt="图片介绍/当图片显示不出来显示这个" title = "悬停文字" width="50px" height="50px"/>
```

## 4.链接标签

```html
<a href="https://www.baidu.com" target="_self">可以嵌套其他的标签</a>
<a href="https://www.baidu.com" target="_blank">可以嵌套其他的标签</a>



<a href= "#qqq"></a>  锚链接 跳到name=qqq的herf.
<a name="qqq"></a>
<a href= "3.html#qqq">跳转到3.html的qqq标签</a>

<a href="mailto:1516156@qq.com">点击联系我</a>  给别人发邮箱
<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=1546546&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:156161:53" alt="点击这里给我发消息" title="点击这里给我发消息"/></a>  qq推广
```

## 5.行内元素和块元素

* 块元素 无论内容多少,该元素独占一行.(p h1-h6)
* 行内元素 内容展开的宽度左右都是行内元素的可以排在一行(a  strong  em)

## 6.列表

* 有序列表

```html
一般用于试卷,问答.....
	<ol>
        <li>java</li>
        <li>java1</li>
        <li>java2</li>
        <li>java3</li>
        <li>java4</li>
    </ol>
```

* 无序列表

![image-20201125165940344](img/image-20201125165940344.png)

```html
第一种带小黑点,一般用于导航,侧边栏.....
	<ul>
        <li>java</li>
        <li>java1</li>
        <li>java2</li>
        <li>java3</li>
        <li>java4</li>
    </ul>
第二种不带小黑点,一般用于公司底部
	<dl>
     	 <dt>介绍</dt>
         <dd>1</dd>
         <dd>2</dd>
         <dd>3</dd>
         <dd>4</dd>
	</dl>
```



## 7.表格

```html
  <table border="2px">
      <th colspan="3">学生成绩</th>
      <tr>
          <td rowspan="2">狂神</td>
          <td>语文</td>
          <td>100</td>
      </tr>
      <tr>
        <td>数学</td>
        <td>100</td>
    </tr>   
    <tr>
        <td rowspan="2">jk</td>
        <td>语文</td>
        <td>100</td>
    </tr>   
    <tr>
        <td>数学</td>
        <td>100</td>
    </tr>
  </table>
```

![image-20201125165902790](img/image-20201125165902790.png)



## 8.视频和音频

* 视频 vidio

* 音频 audio

  ```html
    <audio src="./src/4.mp3" autoplay controls></audio>
    <vidio src="./src/49.mp4" autoplay controls></vidio>
  ```

  ![image-20201125170904300](img/image-20201125170904300.png)

## 9.iframe内联框架

**网页里面内嵌另一个网页.**

```html
 <iframe src="https://www.baidu.com" name="nihao" width="1000px" height="1000px" frameborder="2px"></iframe>
```



![image-20201125171908232](img/image-20201125171908232.png)



<font color = red>**可以让一个页面中的指定部分更新即内嵌的部分更新,不更新全部的页面**</font>

```html
<iframe src="https://www.baidu.com" name="nihao" width="1000px" height="1000px" frameborder="2px"></iframe>
<a href="div.html" target="nihao">点这里</a href>
```



![image-20201125172642127](img/image-20201125172642127.png)

## 10.表单(重点)

### 1.基本属性

![image-20201125180616980](img/image-20201125180616980.png)

```html
    <form action="" method="GET"><!--
        GET方式高效，但是携带的参数比较少，大小有限制，不安全，能从url中看到请求的数据
        POST比较安全，携带的参数没有限制，大小没有限制，不高效，可以传输大文件。
    -->
        姓名：<input type="text" name="username"></input>
        密码：<input type="password" name="pwd"></input>
        <input type="submit">提交</input>
        <input type="radio" value="boy" name="sex">男
        <input type="radio" value="girl" name="sex">女<!--name一样则保持是互斥 提交则传输该数据-->
        <input type="checkbox" name="hobby" id="1" value="sleep">睡觉
        <input type="checkbox" name="hobby" id="2" value="coding">代码
        <input type="checkbox" name="hobby" id="3" value="chat">聊天
        <input type="checkbox" name="hobby" id="4" value="game">游戏
        <input type="image" src="./img/1.jpg" value="跳转"><!--图片也可以提交-->
        <input type="reset" value="重新填写">
            <select name="列表名称" id="2">
                <option value="1">中国</option>
                <option value="2">中国1</option>
                <option value="3">中国2</option>
                <option value="4" selected>中国3</option>
                <option value="5">中国4</option>
            </select>
    </form>
    </form>
```

<hr/>

![image-20201125182307590](img/image-20201125182307590.png)

​        ![image-20201125182340692](img/image-20201125182340692.png)

<hr/>

再加入文本框和上传文件框.

```html
    <form action="" method="GET"><!--
        GET方式高效，但是不安全，能从url中看到请求的数据
        POST比较安全，可以传输大文件。
    -->
        姓名：<input type="text" name="username"></input>
        密码：<input type="password" name="pwd"></input>
        <input type="submit">提交</input>
        <input type="radio" value="boy" name="sex">男
        <input type="radio" value="girl" name="sex">女<!--name一样则保持是互斥 提交则传输该数据-->
        <input type="checkbox" name="hobby" id="1" value="sleep">睡觉
        <input type="checkbox" name="hobby" id="2" value="coding">代码
        <input type="checkbox" name="hobby" id="3" value="chat">聊天
        <input type="checkbox" name="hobby" id="4" value="game">游戏
        <input type="image" src="./img/1.jpg" value="跳转">
        <input type="reset" value="重新填写">
        <body>
            <select name="列表名称" id="2">
                <option value="1">中国</option>
                <option value="2">中国1</option>
                <option value="3">中国2</option>
                <option value="4" selected>中国3</option>
                <option value="5">中国4</option>
            </select>
            建议：<textarea name="advice" id="2" cols="30" rows="10"></textarea><!--这里的advice作为提交的参数名字-->
            <input type="file" name="files" value=""></input><!--这里的files作为提交的参数名字-->
    </form>
```

![image-20201125183207459](img/image-20201125183207459.png)

![image-20201125183343077](img/image-20201125183343077.png)

### 2.验证标签

```html
            <input type="file" name="files" value=""></input><!--这里的files作为提交的参数名字-->
            <input type="email" name="email">
            <input type="number" min="10" max="50">
            <input type="url" name="url">
            音量：<input type="range" name="voice" min="0" max="100" step="10">
            搜索：<input type="search" name="search">
```

![image-20201125184228541](img/image-20201125184228541.png)

### 3.常用属性

* checked 默认选择

* readonly 只读

* disabled 禁用

* hidden <font color='blue'>隐藏该标签 但是还是提交了value</font>

* placeholder 提示信息

  ![image-20201125185700058](img/image-20201125185700058.png)

* required 不能为空

![image-20201125185920733](img/image-20201125185920733.png)

* pattern (模式; 范例; 图案; 模型; 样品)  常与正则表达式一起用   让其内容需要某种格式

  ```html
  <input type="email" name="diyemail" name="email" required pattern="^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$">
  ```

  

![image-20201125190623025](img/image-20201125190623025.png)



### 4.增强鼠标可用性(了解)

```html
<!--让鼠标点姓名:则光标定位到对应的id为username的文本框-->
<label for="username">姓名：</label><input type="text" name="username" id="username"></input>
```

