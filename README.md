# [BluePowerRobotics](https://BluePowerRobotics.github.io)

## 目录

- [BluePowerRobotics](#bluepowerrobotics)
  - [目录](#目录)
  - [所有人必修](#所有人必修)
    - [机器人硬件简介](#机器人硬件简介)
    - [文档写法](#文档写法)
      - [标题：](#标题)
      - [分隔符：](#分隔符)
      - [粗体：](#粗体)
      - [斜体：](#斜体)
      - [列举：](#列举)
      - [制表：](#制表)
      - [插入图片：](#插入图片)
      - [插入链接：](#插入链接)
      - [代码块：](#代码块)
    - [GitHub介绍](#github介绍)
      - [1. 平台性质](#1-平台性质)
      - [2. 核心用户群体](#2-核心用户群体)
      - [3. 主要功能](#3-主要功能)
      - [4. 竞争优势](#4-竞争优势)
      - [5.学习用法](#5学习用法)
  - [各部门必修](#各部门必修)

## 所有人必修

### 机器人硬件简介

| Control Hub | Expansion Hub | Driver Hub | REV SLIM ROBOT BATTERY |
|---|---|---|---|
| ![Control Hub](/RES/ControlHub.png) | ![Expansion Hub](/RES/ExpansionHub.png) | ![Driver Hub](/RES/DriverHub.png) | ![Rev Slim Robot Battery](/RES/Battery.png) |
| 机器人核心部件，用于控制各个执行器（电机、舵机）及传感器（可用手机+EXPANSION HUB代替）。需要使用电池供电；USB-typeC口不可（给CONTROL HUB）供电。 | 用于拓展控制，增加可用舵机、电机数。对于FTC，一辆车最多接12舵机、8电机，因此对于CONTROL HUB只需要且仅允许接入1个EXPANSION HUB（通过RS485接口或MINI USB接口连接） | 连接车辆以执行程序。通过其中Driver Station软件启动。（可用手机代替）使用手柄操控。通过Start+A/B切换第一/二操作手。该软件界面左下部分控制程序运行。该部分顶端显示当前使用程序；按右侧向下三角切换。 | 机器人电源，为设备供电。镍氢电池，无3C标志，并非充电宝，不受新规限制，可以随身携带上飞机。标称电压12V，是12个1.2V电芯串联组成。本身装有（可在国内买到的）保险丝。 |

| 电机 | （普通）舵机 |
|---|---|
| ![REV HD HEX MOTOR](/RES/HdHexMotor.jpg) ![Go Bilda Yellow Jacket Motor](/RES/YellowJacketPlanetaryGearMotor.jpg) | ![DSSERVO](/RES/DSSERVO.png) ![TIANKONGRC](/RES/TIANKONGRC.png) |
| 通过两种线与机器人控制核心连接。电源线提供动力（黑/红），Encoder线获取旋转圈数（红蓝黑白）。特别地，对于Go Bilda电机，均需要特制转接线；这些线应当在购买时与电机配套。如果需要安装在难以拆卸/接线的位置（虽然不建议这么做），请提前将这两种线接好、拉到易于连接的地方。 | （又称为伺服电机）通过三根线（黑/红/白 或 褐/橙/黄）与机器人控制核心连接。对于180、270舵机，信号线（白或黄）向舵机传输角度；对于360舵机，信号线（白或黄）向舵机传输其旋转速度。若想要控制360舵机角度，可考虑磁传感。特别地，无论是何种范围的控制角度舵机，其实际可用角度大概率小于其标定角度：如170/180，255/270。不建议直接通过控制其旋转时间来间接控制角度。需要注意的是，若想要提高效率，工程部成员应当在安装舵机的时候请程电部成员测试/控制其初始角度而非自做主张安装。 |

### 文档写法

本教程采用Markdown标记语言进行编写。

Markdown是一种轻量级的文本标记语言，能够让文档内容通过简单的语法实现排版、美化和结构化，广泛应用于技术文档、博客、项目说明等场景。

常用Markdown语法示例：
#### 标题：

在文本前加#，如`# 一级标题`

```Markdown
# 1
## 2
### 3
#### 4
##### 5
###### 6
```


#### 分隔符：

```Markdown
---
```

#### 粗体：

使用`**加粗内容**`

**加粗内容**

#### 斜体：

使用`*斜体内容*`

*斜体内容*

#### 列举：

使用`-`或`*`加空格

```Markdown
1. 1
2. 2
    - 1
    - 2
        1. a
        2. b
3. 3

- 1
* 2
    * 1
    - 2
* 3
```

1. 1
2. 2
    - 1
    - 2
        1. a
        2. b
3. 3

- 1
* 2
    * 1
    - 2
* 3

#### 制表：

```Markdown
|   1  |  2  |    3 |
|:---:|----:|:----|
|居中|右侧|左侧|
```

|  1   | 2 |  3   |
|:---:|----:|:----|
|居中|右侧|左侧|

#### 插入图片：

```Markdown
![图片描述](图片链接)
```

#### 插入链接：

```Markdown
[链接文字](链接地址)
```

#### 代码块：

用三个反引号包裹代码

```Markdown

    ```Markdown
    # 你好
    ```

```

---

更多语法和用法可参考[Markdown官方文档](https://markdown.com.cn/cheat-sheet.html#总览)。

### GitHub介绍

#### 1. 平台性质

GitHub是一个基于Git的代码托管平台，提供：

- 分布式版本控制
- 云端代码仓库存储
- 协作开发工具套件
- 开发者社交网络功能

#### 2. 核心用户群体

- 软件开发人员（占比约78%）
- 科研人员（特别是计算机相关领域）
- DevOps工程师
- 技术文档撰写者
- 开源项目维护者
- 技术学习者

#### 3. 主要功能

3.1 代码托管

- 支持各种编程语言的仓库
- 提供无限公共仓库（免费账户）
- 私有仓库协作（付费或教育账户）

3.2 协作开发

- Pull Request代码审查机制
- Issue跟踪系统
- Project看板管理
- Wiki文档系统

3.3 自动化

- GitHub Actions持续集成/交付
- 自动化测试部署
- 第三方服务集成

3.4 社区生态

- 开源项目发现与参与
- 技术讨论区
- 开发者社交图谱

#### 4. 竞争优势

4.1 网络效应

- 最大的开发者社区（超过1亿用户）
- 绝大多数知名开源项目选择GitHub

4.2 企业级支持

- GitHub Enterprise解决方案
- 完善的权限管理系统
- 符合企业合规要求

4.3 开发者体验

- 直观的Web界面
- 丰富的API接口
- 强大的搜索功能
- 完善的文档体系

#### 5.学习用法

1. 基础工作流程

1.1 创建仓库
- 点击右上角"+" → "New repository"
- 填写仓库名称/描述
- 选择公开/私有
- 初始化README（推荐）
官方文档：https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository

1.2 基础操作
• 克隆仓库：
```bash
git clone https://github.com/username/repo.git
```
• 提交更改：
```bash
git add .
git commit -m "commit message"
git push origin main
```
官方指南：https://guides.github.com/activities/hello-world/

需要注意的是，可以通过下载`GitHub Desktop`简化操作流程或使用`Github Mobile`直接云端操作。

2. 协作功能详解

2.1 Pull Request流程
1. Fork目标仓库
2. 创建特性分支
3. 提交修改
4. 发起Pull Request
5. 代码审查
6. 合并代码
文档：https://docs.github.com/en/pull-requests

2.2 Issue管理
• 创建：仓库 → Issues → New Issue
• 标签分类
• 分配负责人
• 关联PR
文档：https://guides.github.com/features/issues/

3. 自动化配置（GitHub Actions）

3.1 基础CI/CD
1. 创建.github/workflows目录
2. 编写YAML配置文件
3. 推送触发执行
示例配置：
```yaml
name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - run: make test
```
文档：https://docs.github.com/en/actions

4. 项目管理

4.1 Project看板
• 创建：仓库 → Projects → New Project
• 添加卡片（关联Issue/PR）
• 自定义工作流状态
文档：https://docs.github.com/en/issues/organizing-your-work-with-project-boards

5. 高级功能

5.1 Pages静态网站
• 设置：Settings → Pages
• 选择发布分支
• 自动部署
文档：https://pages.github.com/

5.2 Codespaces云端开发
• 在线VSCode环境
• 预配置开发容器
文档：https://docs.github.com/en/codespaces

建议的学习路径：
1. 先完成基础Hello World教程
2. 实践Pull Request流程
3. 尝试配置基础Actions
4. 参与开源项目协作

## 各部门必修

- [机械程序与电子设计(程电)](/ProgTeam/README.md)

- [机械动力研究设计(工程)](/EngiTeam/README.md)

- [商业宣传与外交联络(商宣)](/BusiTeam/.README.md)