# angular-pcat0
AngularJS Phonecat项目步骤0

最近在学AngularJS的实例教程PhoneCat Tutorial App，发现网上的中文教程都比较久远，与英文版对应不上，而且缺少组件和文件重构两节。所以决定自己整理一个中文简明教程，内容较多，先整理0-5小节。

教程展示一个Angular应用程序：


catalog_screen.png
涉及如下技术：

视图和模型的双向数据绑定；

Karma和Protractor测试；

组件化和模块化编程。

英文教程

配置

安装Git

下载Git，并安装。安装后可以使用git命令行工具git bash，在教程中只用到两个git命令:

git clone ... 从远处版本仓库克隆代码到本地计算机

git checkout ...在本地计算机上查看（取出）特定版本（标签）的代码

拷贝源码

命令行中输入：

git clone --depth=16 https://github.com/angular/angular-phonecat.git
然后打开项目文件：

cd angular-phonecat
注意：从现在开始，所有命令都是在angular-phonecat目录下执行。

安装Node

下载Node.js，并安装。所需Node的最低版本是 Node.js v4+，可以通过下面命令行确认node版本：

node --version
安装工具

npm install
该命令行会安装package.jason规定的工具到node_modules文件夹，并下载AngularJS框架到app/bower_components。

下载的工具有：

Bower - 客户端代码包管理工具

Http-Server - 简单的本地静态web服务器

Karma - 单元测试工具

Protractor - 端到端 (E2E) 测试工具

初步接触项目

npm start: 开启本地服务器

npm test: 运行Karma单元测试工具
单元测试：npm test会自动打开谷歌浏览器和火狐，点击debug、再打开控制台可以查看报错信息。测试成功时，命令行窗口会返回success信息。

npm run update-webdriver: 安装Protractor所需驱动

npm run protractor: 运行Protractor端到端测试
端到端测试：npm run update-webdriver、npm start、npm run protractor。测试成功时，命令行窗口会返回success信息。

注意：输入 npm start 后，应该另外开一个命令行窗口（不能将服务器关闭，否则无法测试），再输入 npm run protractor命令。

0 准备

重置项目

git checkout -f step-0
该命令将重置phonecat项目的工作目录，需要在每一学习步骤运行此命令，将step-0的0改成相应步骤的数字（如：2 AngularJS模板，则数字为2）。

启动服务器

npm start
在浏览器中输入： http://localhost:8000/index.html，查看页面内容。

index.html

app/index.html:

<!doctype html>
<html lang="en" ng-app>
  <head>
    <meta charset="utf-8">
    <title>My HTML File</title>
    <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css" />
    <script src="bower_components/angular/angular.js"></script>
  </head>
  <body>

    <p>Nothing here {{'yet' + '!'}}</p>

  </body>
</html>
代码中，ng-app表示html元素会被Angular用作应用程序的根（root）元素。这就是说，ng-app规定以整个html页面还是部分元素作为Angular程序。

双大括号（Double-curly）绑定表达式:

Nothing here {{'yet'+'!'}}
这一行展示了Angular模板应用的两个核心功能：{{ }}进行绑定，简单表达式'yet'+'!'可以用于绑定。

程序结构如下：


tutorial_00.png

作者：minxuan
链接：http://www.jianshu.com/p/85220c95f3eb
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
