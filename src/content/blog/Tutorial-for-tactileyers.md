---
author: Leilei Xia
pubDatetime: 2023-12-29T21:39:36+00:00
title: 如何更新文章
postSlug: Tutorial-for-tactileyers
featured: true
draft: false
tags:
  - tutorial-教程
  - Tactileye-organization-触目组织
description: 教你如何在触目上更新文章
---

这个教程是给触目例会成员，以及其他想要在触目网站上发表文章的朋友使用的指南。虽然长度很长，但是其实只是因为介绍了好几种不同的可以平替的方式罢了。大家可以通过选择"Table of Contents"查看目录以及跳转到合适的位置。

## Table of Contents

## 第一步：注册账号、获得权限

首先，触目的网站内容是寄托在 [Github](https://github.com) 上面的。虽然 Github 的库是公开的，但是想要在上面编辑内容，你需要注册一个 GitHub 账号，然后询问管理员要 [这个repository](https://github.com/Tactileye/Tactileye-astro-paper) 的权限。

P.S. 使用github有可能需要魔法上网。如果你有触目官方的 github 账号和密码，也可以自己操作转移权限。

## 第二步：获得触目网站数据库

你有三种方式来获得触目的网站数据库，选择其中一种就好。如果你嫌麻烦，我会推荐在线编辑器，可以直接跳到方式三。

### 方式一：Github客户端

其中一种方式是[github的客户端](https://desktop.github.com)，登陆之后你可以克隆一份触目网站的repository到你的本地电脑上。

具体就是你在登陆后，来到 Github 客户端左上角，点击“add/添加”，然后在下拉菜单里选择“Clone Repository/克隆储存库”

![屏幕截图：在add的下拉菜单里找到“克隆你的repository”](https://media.discordapp.net/attachments/1190410492691365908/1190410554104348682/Screenshot_2023-12-29_at_4.46.29_PM.png?ex=65a1b338&is=658f3e38&hm=aa162a8ea96873efe20004c6315519d9980e80e93510a71b973717ffe8d0f3b2&=&width=1648&height=596)

然后会跳出一个窗口，让你选择克隆哪个库。如果你已经是这个repository/库 的 collaborator/合作者, 那你应该会看到在Tactileye的一栏下面会有一个 Tactileye-astro-paper 的库，选择这个。这个就是触目整个网站的数据库。

在下面的 Local Path/本地路径 选择你希望把触目的数据库保存在哪儿。注意需要选择一个完全空的文件夹。

![屏幕截图：选择触目的repository进行克隆](https://media.discordapp.net/attachments/1190410492691365908/1190411043952918649/Screenshot_2023-12-29_at_4.48.24_PM.png?ex=65a1b3ad&is=658f3ead&hm=c575e15efc5aad03c232e0aeacd8a59f5a03a89cba425e21dc7a1b64f238e089&=&width=1194&height=1178)

### 方式二：Git

Git会比较硬核一点，但是一旦设置好了也会比较轻松。

1. 安装 Git

   首先，你需要在你的计算机上安装 Git。你可以访问 Git 官网 来下载适用于你操作系统的 Git 版本。安装过程中，你可以接受大多数默认设置。

2. 配置 Git

   安装完成后，打开终端（在 Windows 上是命令提示符或 PowerShell），输入一下信息，然后回车：

   ```bash
   git config --global user.name "你的名字"
   git config --global user.email "你的邮箱"
   ```

   注意请把里面的你的名字、你的邮箱都替换成你自己的

   这些信息会用在你的提交（commit）上。

3. 克隆我们的仓库

   如果你想要在本地工作一个已经存在的远程仓库，可以使用 git clone 命令：

   ```bash
   git clone https://github.com/Tactileye/Tactileye-astro-paper.git
   ```

   这会将远程仓库复制到你的本地机器上。如果你想确保你配置好了，也可以输入一下命令。

   ```bash
   git remote add origin https://github.com/Tactileye/Tactileye-astro-paper.git
   ```

方式一和方式二都是本地部署文件夹的。如果是是用这样的方式，你需要做以下的步骤：

1. 来到你的文件夹(叫 "tactileye-astro-paper" 的文件夹)
2. 文件夹里，找到一个叫"src"的文件夹，里面有一个叫“content"的文件夹，然后这里面有一个叫"blog"的文件夹
   ![截图：找到名字叫"blog"的文件夹](https://media.discordapp.net/attachments/1190410492691365908/1190752565755908217/Screenshot_2023-12-30_at_3.25.30_PM.png?ex=65a2f1be&is=65907cbe&hm=95d1d456052e3d77cab1050a032a7a1f0dc6be4349c442a6f36eb05dfead2b7a&=&width=1090&height=1178)
3. 你可以在这个文件夹里添加新的文章——**注意**，文件的格式必须是[Markdown](https://www.markdownguide.org/basic-syntax/)格式的，也就是文件是以“.md"结尾的。Markdown是一种比较普遍用于写程序教程文档的一种语言，可以进行比较简单统一的文字格式风格。你选择使用你喜欢的文本编辑器或者编译软件，我一般使用[VScode](https://code.visualstudio.com), 如果是这样的话你可以把这个文件夹直接拖进VScode里。
   你也可以选择使用别的，使用txt编辑器都可以。

### 方式三：在线文件夹

和本地文件相似，你也可以在线用一些平台对github里的文件进行编辑。我比较推荐的是[github.dev](http://Github.dev)。这个方法你就不需要在本地部署文件夹同步了。

1. 直接来到[blog 文件夹](https://github.com/Tactileye/Tactileye-astro-paper/tree/main/src/content/blog)，点击左边的链接即可。

2. 可以直接点击这个链接进入示例post的在线编辑地址：[sample-post.md](https://github.dev/Tactileye/Tactileye-astro-paper/blob/main/src/content/blog/sample-post.md) 然后你就可以跳到第三步了。
   当然你也可以自己从零开始新建一个文件，具体步骤如下：
   
   a. 你可以点击右侧Add File新建一个文件
   ![新建文件，或者上传文件都可以](https://media.discordapp.net/attachments/1190410492691365908/1190776001257549854/Screenshot_2023-12-30_at_4.58.37_PM.png?ex%253D65a30792%2526is%253D65909292%2526hm%253Dd836381605bf752135d4d09ca2a4ab4f1aee005bf192fe381c6b1935921e5a3f%2526%253D%2526width%253D824%2526height%253D528)
   注意你需要输入你新建的文件的名字，需要是.md结尾的
   ![你的文件名.md](https://media.discordapp.net/attachments/1190410492691365908/1190776281877458984/Screenshot_2023-12-30_at_4.59.43_PM.png?ex%253D65a307d5%2526is%253D659092d5%2526hm%253D59638c6313038b4f391365532785280c9c79252f282e10bffafffd89fb505403%2526%253D%2526width%253D2476%2526height%253D184)
   b. 然后选择commit changes，在新的文件页面右侧的小工具栏里选择用github.dev打开
   ![选择open with github.dev](https://media.discordapp.net/attachments/1190410492691365908/1190776905402687488/Screenshot_2023-12-30_at_5.02.13_PM.png?ex%253D65a30869%2526is%253D65909369%2526hm%253Daf5983c95b78a9c8a7aa8f3d31dc4dae4eb435b6dea8c615590851a537627577%2526%253D%2526width%253D1148%2526height%253D1048)
   

## 第三步：开始编辑

1. 在文章的开头，你需要添加一个YAML Formatter，这个是可以告诉我们的数据库你这个文章的一些metadata（元数据），就是关于它的一些信息，有助于网站的生成。例如：

   ```yaml
   # src/content/blog/sample-post.md
   # 这里面井号后面的字都是评论和注释
   --- #这里和下面三条杠都是必须要的，而且这一部分应该放在文章的开头。
   title: 你的文章标题
   author: 你的名字
   pubDatetime: 2022-09-21T05:17:19Z
   slug: the-title-of-the-post
   #slug代表的是这个网址会显示什么内容，一般就是一个后缀，所以这里面的文字*不要包含空格*。例如：a workshop 应该改为 a-workshop
   featured: true
   # 就是你的文章是否出现在首页上
   draft: false
   #如果draft是true的话，你的文章只会保存在数据库里，2而不会出现在网站的任何地方
   tags:
     - 一些
     - 案例
     - 标签
   # tags可以参考之前有过的tags，例如“documentation-回顾”，“tutorial-教程“。已经有的tag就不要创建一个新的但是其实是一样的tag了
   ogImage: ""
   description: 一个简短的介绍，会出现在网站的预览里
   ---
   ```

2. 做完这一步，你就可以开始编辑了。如果你了解了一点markdown，你会知道可以通过打井号来直接生成标题，例如：

   ```markdown
   ## 二级标题
   ```

   需要注意的是井号后面的空格也是必须要的。效果就是如下：

   ## 二级标题

   但是需要注意的是，因为我们的文章标题已经在formatter里写好了，所以你写文章是从二级标题开始写，也就是从两个井号开始。

P.S.

另一个重要的技巧就是添加图片。代码类似下面这样：

```markdown
![图片描述](图片的链接,xxx.jpg,最好是一个在网上的图片地址)
```

效果如下：

![示例图片](https://media.discordapp.net/attachments/1069687619056832622/1094286434447409262/WechatIMG74.jpeg?ex=65a2afa8&is=65903aa8&hm=5f3a263bc6bcc60907142d8beff158df62439db5f2ef369717b2b3124aa849f7&=&width=1768&height=1178)

需要注意的是，触目的文章都需要有图片描述，方便视障读者阅读。需要注意的是即便你的描述不会出现在图片上，读屏用户也是能读到的。你就不需要额外的图片描述了，除非你有一些别的信息可以补充的。

关于图片的链接，你可以把图片先发到网上，然后复制图片地址到那个括号里。如果你能够使用 [Discord](https://discord.com) （一个聊天平台），可以询问触目的discord管理员把你添加入discord群，你可以把图片发到那里，discord会生成一个永不过期的图片地址。只要是小于25M的都可以发送。（质量也相当高的）

不推荐把图片直接放到我们的数据库里！容量有限可能会爆炸！

## 最后一步：上传到数据库

你已经做好了编辑。如果你是在本地编辑的，那么你还需要有一步就是上传回github里。

### 方式一：使用Github客户端

1. 当你编辑完并且保存之后之后，你会看到你的github客户端已经会显示你修改的很多内容了

   ![截图：github客户端上会显示你修改了哪些内容](https://media.discordapp.net/attachments/1190410492691365908/1190764950944235642/Screenshot_2023-12-30_at_4.14.44_PM.png?ex=65a2fd47&is=65908847&hm=4223a24b11d933fef3ad7cc50bde78fb6a63073b3ef09cfcdeafb487b812c640&=&width=1720&height=1178)

2. 在左下角输入你的标题和描述信息，是告诉我们你这次提交是什么主题的，以及描述一下你提交的内容
   ![截图：写你的提交主题和描述](https://media.discordapp.net/attachments/1190410492691365908/1190765750433091704/Screenshot_2023-12-30_at_4.17.52_PM.png?ex=65a2fe06&is=65908906&hm=4f7b0d3f2f8895a671078c91c3f94105e4e5593ec4845ccf56be282515abf74a&=&width=996&height=800)
3. 点击下方的"Commit to main"或者“提交到主库”
4. 不要忘记！你还得点击右上角的 Push origin，也就是推送出去。不然你的文章是不会出现在网站上的！
   ![记得要推送出去！要push！](https://media.discordapp.net/attachments/1190410492691365908/1190766218404171836/Screenshot_2023-12-30_at_4.19.44_PM.png?ex=65a2fe75&is=65908975&hm=fd7cb2132dee680dfef6b3b6eb806dd60db1a16a261106df27f694bed3116a94&=&width=2476&height=254)

### 方式二：使用Git

1. 添加文件

   在你的仓库中创建或修改文件后，你需要使用 git add 命令将它们添加到暂存区：

   ```bash
   git add <文件名>
   ```

   或者使用

   ```
   git add .
   ```

   可以添加所有更改过的文件。上面那个逗号是英文逗号，而且和add之间隔了一个空格。

1. 提交更改

   要将这些更改保存到仓库的历史记录中，你需要进行提交：

   ```
   git commit -m "提交信息"
   ```

   请一定记得写你提交信息的一行描述……不然代码会追着你不放很烦的。

1. PUSH!!

   这样你可以提交你的代码，但这不代表它就更新了。要把代码push到原来的库上，你需要输入下面的命令：

   ```
   git push
   ```

### 方式三：在线编辑器（以github.dev为例）&& VScode

如果你是使用GitHub dev，它的界面会和vscode比较相似，所以你也可以在VScode里是用这样的技巧。你会在侧边拦找到一个叫Source Control的按钮，或者是源管理。
![源管理里面会显示你修改的文件，点击Commit & Push](https://media.discordapp.net/attachments/1190410492691365908/1190778821549490347/Screenshot_2023-12-30_at_5.09.50_PM.png?ex%253D65a30a32%2526is%253D65909532%2526hm%253Deb554f69984cadcb9d8b3b375ca1879cf60bb26247550147e50502547668a747%2526%253D%2526width%253D1372%2526height%253D776)

源管理里面会显示你修改的文件，填写你的提交message，然后点击Commit & Push就可以一气呵成地提交数据库了。当然，你也可以选择先commit然后再push。

然后就大功告成了！过几分钟刷新网站，你的文章就会出现在页面里了
