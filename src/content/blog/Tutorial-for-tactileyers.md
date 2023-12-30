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

## 注册账号、获得权限

首先，触目的网站内容是寄托在 [Github](https://github.com) 上面的。虽然 Github 的库是公开的，但是想要在上面编辑内容，你需要注册一个 GitHub 账号，然后询问管理员要 [这个repository](https://github.com/Tactileye/Tactileye-astro-paper) 的权限。

P.S. 使用github有可能需要魔法上网。如果你有触目官方的 github 账号和密码，也可以自己操作转移权限。

## 获得你的本地文件夹

### Github客户端

其中一种方式是[github的客户端](https://desktop.github.com)，登陆之后你可以克隆一份触目网站的repository到你的本地电脑上。

具体就是你在登陆后，来到 Github 客户端左上角，点击“add/添加”，然后在下拉菜单里选择“Clone Repository/克隆储存库”

![屏幕截图：在add的下拉菜单里找到“克隆你的repository”](https://media.discordapp.net/attachments/1190410492691365908/1190410554104348682/Screenshot_2023-12-29_at_4.46.29_PM.png?ex=65a1b338&is=658f3e38&hm=aa162a8ea96873efe20004c6315519d9980e80e93510a71b973717ffe8d0f3b2&=&width=1648&height=596)

然后会跳出一个窗口，让你选择克隆哪个库。如果你已经是这个repository/库 的 collaborator/合作者, 那你应该会看到在Tactileye的一栏下面会有一个 Tactileye-astro-paper 的库，选择这个。这个就是触目整个网站的数据库。

在下面的 Local Path/本地路径 选择你希望把触目的数据库保存在哪儿。注意需要选择一个完全空的文件夹。

![屏幕截图：选择触目的repository进行克隆](https://media.discordapp.net/attachments/1190410492691365908/1190411043952918649/Screenshot_2023-12-29_at_4.48.24_PM.png?ex=65a1b3ad&is=658f3ead&hm=c575e15efc5aad03c232e0aeacd8a59f5a03a89cba425e21dc7a1b64f238e089&=&width=1194&height=1178)

### Git

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

## 找到文件夹和选择编辑器

### 本地文件夹

1. 当你下载好了文件之后，来到你的文件夹(一个叫tactileye-astro-paper的文件夹)
2. 文件夹里，找到一个叫"src"的文件夹，里面有一个叫“content"的文件夹，然后这里面有一个叫"blog"的文件夹
   ![截图：找到名字叫"blog"的文件夹](https://media.discordapp.net/attachments/1190410492691365908/1190752565755908217/Screenshot_2023-12-30_at_3.25.30_PM.png?ex=65a2f1be&is=65907cbe&hm=95d1d456052e3d77cab1050a032a7a1f0dc6be4349c442a6f36eb05dfead2b7a&=&width=1090&height=1178)
3. 你选择使用你喜欢的文本编辑器或者编译软件，我一般使用[VScode](https://code.visualstudio.com), 如果是这样的话你可以把这个文件夹直接拖进VScode里。
   你也可以选择使用别的，使用txt编辑器都可以。那样你就新建一个文件，但是*文件后缀名一定得是.md格式*的。

### 在线文件夹

和本地文件相似，你也可以在线用一些平台对github里的文件进行编辑。我比较推荐的是github.dev,你登陆之后，一开始是会给你来到一个叫github/dev的文件夹，你要去到上两级的文件夹，知道你看到你的用户名和tactileye的用户名，选择tactileye的名字，然后你就可以找到这个库了。之后的流程和本地文件夹一样。

## 进行编辑

1. 你可以在这个文件夹里添加新的文章——**注意**，文件的格式必须是[Markdown](https://www.markdownguide.org/basic-syntax/)格式的，Markdown是一种比较普遍用于写程序教程文档的一种语言，可以进行比较简单统一的文字格式风格。
2. 在文章的开头，你需要添加一个YAML Formatter，这个是可以告诉我们的数据库你这个文章的一些metadata（元数据），就是关于它的一些信息，有助于网站的生成。例如：

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

做完这一步，你就可以开始编辑了。如果你了解了一点markdown，你会知道可以通过打井号来直接生成标题，例如：

```markdown
## 二级标题
```

需要注意的是井号后面的空格也是必须要的。效果就是如下：

## 二级标题

但是需要注意的是，因为我们的文章标题已经在formatter里写好了，所以你写文章是从二级标题开始写，也就是从两个井号开始。

另一个重要的技巧就是添加图片。代码类似下面这样：

```markdown
![图片描述](图片的链接,xxx.jpg,最好是一个在网上的图片地址)
```

效果如下：

![示例图片](https://media.discordapp.net/attachments/1069687619056832622/1094286434447409262/WechatIMG74.jpeg?ex=65a2afa8&is=65903aa8&hm=5f3a263bc6bcc60907142d8beff158df62439db5f2ef369717b2b3124aa849f7&=&width=1768&height=1178)

需要注意的是，触目的文章都需要有图片描述，方便视障读者阅读。需要注意的是即便你的描述不会出现在图片上，读屏用户也是能读到的。你就不需要额外的图片描述了，除非你有一些别的信息可以补充的。

关于图片的链接，你可以把图片先发到网上，然后复制图片地址到那个括号里。如果你能够使用 [Discord](https://discord.com) （一个聊天平台），可以询问触目的discord管理员把你添加入discord群，你可以把图片发到那里，discord会生成一个永不过期的图片地址。只要是小于25M的都可以发送。（质量也相当高的）

不推荐把图片直接放到我们的数据库里！容量有限可能会爆炸！

## 上传到数据库

你已经做好了编辑。如果你是在本地编辑的，那么你还需要有一步就是上传回github里。

### 使用Github客户端

1. 当你编辑完并且保存之后之后，你会看到你的github客户端已经会显示你修改的很多内容了

   ![截图：github客户端上会显示你修改了哪些内容](https://media.discordapp.net/attachments/1190410492691365908/1190764950944235642/Screenshot_2023-12-30_at_4.14.44_PM.png?ex=65a2fd47&is=65908847&hm=4223a24b11d933fef3ad7cc50bde78fb6a63073b3ef09cfcdeafb487b812c640&=&width=1720&height=1178)

2. 在左下角输入你的标题和描述信息，是告诉我们你这次提交是什么主题的，以及描述一下你提交的内容
   ![截图：写你的提交主题和描述](https://media.discordapp.net/attachments/1190410492691365908/1190765750433091704/Screenshot_2023-12-30_at_4.17.52_PM.png?ex=65a2fe06&is=65908906&hm=4f7b0d3f2f8895a671078c91c3f94105e4e5593ec4845ccf56be282515abf74a&=&width=996&height=800)
3. 点击下方的"Commit to main"或者“提交到主库”
4. 不要忘记！你还得惦记

### 使用Git

1. 添加文件

在你的仓库中创建或修改文件后，你需要使用 git add 命令将它们添加到暂存区：

```bash
git add <文件名>
```

使用 `git add .` 可以添加所有更改过的文件。

2. 提交更改

要将这些更改保存到仓库的历史记录中，你需要进行提交：

```
git commit -m "提交信息"
```

这样你可以提交你的代码，但这不代表它就更新了。要把代码push到原来的库上，你需要输入下面的命令：

```
git push
```

然后就大功告成了！过几分钟刷新网站，你的文章就会出现在页面里了
