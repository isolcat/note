# 一些html中常见的语法：

## 文字效果：

### <p></p>为段落标签

### <b></b>为加粗文字  

### <em></em>为倾斜文字

### <del></del>为删除线

### <ins></ins>为下划线

### <div></div>div标签独占一行 

### <span></span>span标签表示为空格  用于文字和文字之间

## 图像标签：

###  <img src="" alt="">其中src后面跟图像的地址（如 <img src="img.jpg" />）

### **alt为“替换文本”当图像显示不出来的时候使用文字进行替换**

<!--如果想要让鼠标放在图片上就显现出文字不能使用alt 应该在后面再加上title=“”-->

（例如<img src="img.jpg" title="我是雪之下雪乃" />）

## 路径：

### 同一级路径：<img src="img.jpg">直接写文件名即可

### 绝对路径： 如    <img src="C:\Users\HSDN\Desktop\前端HTML\img.jpg" />



或者    <img src="https://i0.hdslb.com/bfs/feed-admin/7c997bce21ee896fc2552e56ea783591a6e7ede8.png" />

直接写出网址或者该图片所在的网盘位置

## 超链接标签：

​    <a href="http://www.qq.com" target="_blank">腾讯</a>
其中 **target** 打开窗口的方式 默认的是**_self**在当前页面打开 **_balnk**是在一个新的页面打开

## 注释和特殊字符：

<!--我想喝星巴克的丝滑拿铁-->

也可以在vscode中使用快捷标签如ctrl+/

#### 特殊字符参考https://www.runoob.com/html/html-entities.html

## 表格

    <table>
        <tr>
            <th>姓名</th>
            <th>性别</th>
            <th>年龄</th>
        </tr>
        <tr>
            <td>雪之下雪乃</td>
            <td>女</td>
            <td>16</td>
        </tr>
    </table>

## 列表（无序列表 有序列表 自定义列表）：

#### 无序列表：

  `<ul>`

​    `<!-- ul里面只能放li标签 li中可以放任何元素 -->`

​    `<li>榴莲</li>`

​    `<li>臭豆腐</li>`

​    `<li>`

            <p>123</p>

​    `</li>`

  `</ul>`

可以使用快捷键：**ul>li*n**(n是你想要使其出现的li的个数)

例如ul>li*3（会出现三个li）

#### 有序列表：

  `<ol>`

​    `<li>刘德华</li>`

​    `<li>pink老师</li>`

  `</ol>`

`</body>`

<!-- 有序列表会自带属性，但在实际使用中会用css来设置 -->

在实际开发中我们会通过css来去掉其小圆点 他的语法和无序列表一样（**ol>li*3**）

#### 自定义列表：

  `<dl>`

​    `<dt>关注我们</dt>`

​    `<dd>新浪微博</dd>`

​    `<dd>微信公众号</dd>`

  `</dl>`

<!-- dl里面只只能包含dt和dd 对dt和dd的数量没有限制 dt和dd里面可以放任何标签-->

## 表单域和表单元素：

#### 表单域：  <form acyion="demo.php" method="POST" name="namel"></form>

#### 表单元素：  <form action="xxx.php" method="get">

​    <!-- text 文本框 用户可以在里面输入任何文字 -->

​    <!-- maxlength可以输入的最大长度 -->

​    用户名：<input type="text" name="username" value="请输入用户名" maxlength="6"> <br> 密码：

​    <input type="password" name="pwd"><br>

​    <!-- name 是表单元素名字 这里的性别单选按钮必须有相同的名字name才可以单选 -->

​    <!-- 密码不能让用户看见 应该用**来展现出安全性 -->

​    <!-- radio 单选按钮 可以多选一 -->

​    <!-- 单选按钮和复选框可以设置check属性 在页面打开的时候默认勾选这个按钮 -->

​    性别：男 <input type="radio" name="sex" value="男" checked="checked">女<input type="radio" name="sex" value="女">

​    <!-- checkbox 复选框 可以实现多选 -->

​    <br> 爱好：二次元 <input type="checkbox" name="hobby"> 鞋圈<input type="checkbox" name="hobby"> 饭圈<input type="checkbox" name="hobby"> 科技

​    <input type="checkbox" name="hobby"> 政治<input type="checkbox" name="hobby"> 体育<input type="checkbox" name="hobby">

​    <!-- name和value是用于给后台人员使用的 -->

​    <!-- 单选按钮和复选框都要有相同的name -->

​    <br>

​    <input type="submit" value="免费注册"><br>

​    <input type="reset" value="重新填写"><br>

​    <!-- 重置按钮reset可以还原表单的默认状态 -->

​    <input type="button" value="获取短信验证码"><br>

​    <!-- 后期结合js使用 -->

​    <!-- 文件域 上传文件的时候使用 -->

​    上传头像：<input type="file">

  </form>

  <!-- 点了提交按钮就可以把表单域from里面的表单元素里面的值提交给后台服务器 -->

## 标签名：

 <label for="text">用户名：</label><input type="text" id="text">

  <input type="radio" id="man"><label for="man">男</label>

**HTML `<label>` 元素（标签）**表示用户界面中某个元素的说明。

<div class="preference">
    <label for="cheese">Do you like cheese?</label>
    <input type="checkbox" name="cheese" id="cheese">
</div>

<div class="preference">
    <label for="peas">Do you like peas?</label>
    <input type="checkbox" name="peas" id="peas">
</div>

## 下拉表单：

  <select>

​    <option>四川</option>

​    <option>北京</option>

​    <option selected="selected">上海</option>

​    <option>江苏</option>

​    <option>广东</option>

  </select>

![image-20210807112201946](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210807112201946.png)**如图所示**

## 文本域：

  <form>

​    今日反馈：

​    <textarea cols="50" rows="5">pink老师,我知道这个反馈留言是用textarea做的

​    </textarea>

  </form>

**效果如图所示**![image-20210807112459825](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210807112459825.png)

**cols是设置textarea的宽度** 

**rows是设置textarea的高度**（均不用带单位px）
