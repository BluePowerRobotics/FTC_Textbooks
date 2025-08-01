# GitHub协作介绍

## 目录

- [GitHub协作介绍](#github协作介绍)
  - [目录](#目录)
  - [总览](#总览)
  - [简介](#简介)
  - [用法](#用法)
  - [一些规范](#一些规范)

## 总览

在本页中，你将会了解到如何通过**github**与他人合作完成代码。但是，~~由于编写者精力有限~~由于自学对于程序编写者是一个必不可缺的过程（编者所写内容也均为自学而来），本页面不会对可能遇到的问题、具体的流程、（可能的）相关的繁琐步骤作出详细说明。

## 简介

> GitHub是一个程序员的社交软件。
>
> ——《GitHub漫游手册》

(在GitHub中搜索`GitHub漫游手册`以查看完整内容)

通过GitHub，你可以：

- 探究前沿技术（如DeepSeek开源项目、探究FFmpeg对性能的极致优化）、
- 聊天八卦（如最近某Linux开源项目中一文件系统功能编写者与负责人吵架）、
- 释放灵感（任何人都可以创建开源/闭源存储库）、
- 保护著作权（每个存储库都可以单独设置许可证）
- 获得更加便利的工具（比如MacOS上的HomeBrew——软件包管理器，Unix系统上的Wine——Windows兼容层）

等等。

对于FTC比赛，使用GitHub作为远程托管服务平台是非常有优势的。

首先，我们的母仓库（指的是比赛所需代码环境）在GitHub上；

GitHub上有很多其他队伍的优秀案例；

GitHub广告少，界面清爽，下载便捷（点名批评Gitee）；

GitHub上有许多我们所需要的插件（比如RoadRunner）

......等等。

纵使它也有缺陷——比如网速慢，但瑕不掩瑜，在最后，我们选择了GitHub。

## 用法

GitHub官网是：[GitHub.com](https://github.com)。

访问其官网并点击右上角注册。

搜索栏中可以搜索（非常明显，对吧？），点自己头像可以修改信息，邮件按钮可以收到站内消息（比如组织邀请、Pull Request等等）。

GitHub Copilot是（非常好用的）AI工具，可以访问gpt4等等工具。具有免费额度。（正常使用都是够的）

建议配套github desktop使用。其图形化的界面简洁直观，且在对github的网络链接上表现稳定。
下载链接：https://desktop.github.com/download/

看到喜欢的存储库，不妨点个Star，就像点赞一样。

想要修改一个没有权限的存储库，可以点击Fork——或者说，复刻——在你的账户或你所属的组织账户下复制一份可以收到原项目更新的存储库；随后修改，commit（本地），push（上传），pull request（提交审核）。

如果你具有权限——你和你的同伴在同时修改一个存储库。为了不互相影响——不妨创建分支（branch）。你在你的分支修改，我在我的分支修改。写完一个功能，merge进main分支。

简单来说，就是这样。


## 一些规范

1：每次push前请先本地commit并pull（先stash，在pull之后恢复也可），检查有无兼容性问题，不要提交会导致编译/运行错误的代码。

2：每次commit需在提交标题中注明提交日期，提交人，修改内容（不必非常具体，一句话即可，有利于后续检索）


这是一个很好的例子“722 gyb update ColorSensorDetector, colorSensorTest”


3：一般情况下所有人均在master内工作即可，建议每天工作结束就提交一次。但如果对某些分功能（e.g. 视觉、机械臂）进行长期、单人的工作时也可以新建分支。
