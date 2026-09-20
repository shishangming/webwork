# HTML用户注册登录综合实验
## 项目说明
本项目完成用户注册、登录页面的制作，实现多页面跳转交互。一共包含4个网页文件，全部遵循HTML5语义化开发规范，满足实验各项考核要求。

## 文件列表
- index.html：首页（注册须知页面，底部有登录、注册跳转按钮）
- register.html：用户注册页面，完整表单，提交后跳转登录页
- login.html：用户登录页面
- success.html：登录成功提示页面

## 使用主要标签与知识点
1. 语义化标签：`<header>`、`<main>`、`<footer>`，构建页面标准结构
2. 列表标签：`<ul>`无序列表、`<ol>`有序列表、`<dl>/<dt>/<dd>`定义列表
3. 表格标签：`<table>`、`<thead>`、`<tbody>`、`<tr>`、`<th>`、`<td>`，使用`colspan`实现单元格合并
4. 表单控件：text、password、radio、checkbox、date、email、tel、file、select、textarea
5. label两种实现方式：for+id绑定、标签包裹input
6. 表单校验属性：`required`必填校验、`pattern`正则校验手机号
7. JavaScript知识点
    - submit表单提交事件监听
    - `e.preventDefault()`阻止表单默认刷新
    - FormData获取表单全部数据，控制台打印输出
    - location.href实现页面之间相互跳转

## 页面业务流程
1. 打开`index.html`首页
    - 点击【登录】按钮，跳转到login.html登录页面
    - 点击【注册】按钮，跳转到register.html注册页面
2. register.html注册页面
    填写表单信息，点击注册按钮，完成注册逻辑，自动跳转登录页面login.html
3. login.html登录页面
    输入信息点击登录，跳转success.html登录成功页面
4. success.html成功页，提供返回首页按钮，回到index.html

## 遇到的困难以及解决方法
1. label点击无效果：区分两种写法，一种通过id与for关联；另一种直接把input嵌套在label内部。
2. 表单提交页面直接刷新：使用`e.preventDefault()`阻止浏览器表单默认提交行为，才可以打印表单数据以及实现页面跳转。
3. 多页面跳转出现404：所有html文件放置在同一个文件夹，文件名大小写保持一致。
4. 复选框获取数据：多个复选框设置同一个name属性，FormData对象遍历读取值。

## 运行方式
1. 将全部4个html文件放在同一个文件夹。
2. 使用VSCode，安装Live Server插件。
3. 右键打开`index.html` → Open with Live Server。
4. F12打开浏览器控制台Console面板，填写表单提交，查看输出的表单数据。

## 实验要求核对
✅ header、main、footer语义标签
✅ 表格单元格合并colspan
✅ ul、ol、dl三种列表
✅ 全部表单控件、name属性齐全
✅ required、pattern表单校验
✅ label两种写法
✅ JS收集打印表单数据
✅ 多页面之间跳转交互
✅ 代码小写，属性使用双引号，缩进整齐规范
