<div align="right">
  Language:
  cn
</div>

# TMS little helper

<p align="center">
    <a href="https://github.com/Tikas/TMS-little-helper/LICENSE">
        <img alt="GitHub" src="https://img.shields.io/github/license/Tikas/TMS-little-helper"/>
    </a>
    <a href="https://github.com/Tikas/TMS-little-helper">
        <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Tikas/TMS-little-helper"/>
    </a>
    <a href="https://github.com/Tikas/TMS-little-helper/releases">
        <img alt="GitHub release (latest by date including pre-releases)" src="https://img.shields.io/github/v/release/Tikas/TMS-little-helper?include_prereleases&sort=semver&style=flat-square"/>
    </a>
    <a href="https://github.com/Tikas/TMS-little-helper/releases">
        <img alt="GitHub all releases" src="https://img.shields.io/github/downloads/Tikas/TMS-little-helper/total"/>
    </a>
</p>

<p align="center">
    <a href="https://xtikas.com/tms-little-helper">
        <img alt="TMS little helper home page" src="https://img.shields.io/badge/HomePage-TMS小帮手-blue.svg"/>
    </a>
</p>

![Status](https://repobeats.axiom.co/api/embed/c65e9372e59dbf80f59b3e35a8a1dfc34ae343a0.svg)

文档：📖 撰写中...

一个致力于 TMS (TW MapleStory) 更好的启动、登录、多账号管理等相关解决方案。

## 本项目暂时搁置

突发情况，因某客户要求，强制某商业项目需要在 9 月前完成。

现在不得不需要全心全意计划一个月内完成客户项目，并保证一个月后有多余的时间测试。

为此，此项目暂时停下开发。

## 🖥️ 使用

### 下载

前往 [https://github.com/Tikas/TMS-little-helper/releases](https://github.com/Tikas/TMS-little-helper/releases) 下载最新版本

### 使用环境

TMS little helper 本身无需任何运行库即可运行，但是使用了一些第三方工具会需要以下运行库，请确保电脑的操作系统已安装。

使用的第三方工具列表：

- [Locale Remulator 系统区域和语言模拟器](https://github.com/InWILL/Locale_Remulator)
- [Pungin 的 DES 源码构建 DES.dll](https://github.com/pungin/Beanfun/blob/code/Beanfun/API/WCDESComp.cs)

Locale Remulator 核心 Dll 必需使用 Microsoft Visual C++ Redistributable 运行库：

[vs 2015-2022 x64 运行库](https://aka.ms/vs/17/release/vc_redist.x64.exe) | [vs 2015-2022 x86 运行库](https://aka.ms/vs/17/release/vc_redist.x86.exe)

Locale Remulator 调用程序以及 DES.dll 必需要使用 .NET Framework 4.8 运行库：

[.NET Framework 4.8 运行库](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net48-web-installer) Windows 10 + 已经自带，不需要再安装，Windows 7 用户需要安装

### 使用过程所需要的相关文件

TMS little helper 会在以下位置存放一些文件：

- C:\Users\电脑的用户名\AppData\Local\tikas
  - 主要存放配置文件（加密），以及 LR 转区工具
- C:\Windows\system32
  - 随机目录创建随机文件及随机文件名，主要存放两个加密文件，一个是：账号信息文件；另一个是：账号所对应的密码文件。
- 在注册表：HKEY_LOCAL_MACHINE\SOFTWARE\Classes\apphelper 创建 app 记录随机码

本程序加密强度大，删除配置文件，或者，删除注册表记录的随机码，将会导致账号信息、密码文件无法正常解读。

加密文件使用高强度密码加密，账号的密码更是使用登录前解锁的 6 位主密码进行加密，此密码请不要告诉别人，这是最后的防线！

## 🎉 特色

- [x] 更加安全：强制使用 6 位主密码，没有正确的密码不允许解锁使用，以防止远程电脑时所有账号信息不设防
- [x] 更加安全：加密使用电脑特征码 + 随机码 + 6 位主密码进行高强度加密
- [x] 更加安全：账号记录信息和密码记录信息分开存放，并且使用随机存放
- [x] 更加安全：所有保存的账号全部强制转换 BFM 账号并以此账号登录，是否记住原始账号（如 Email）看个人需求，如记录，此账号仅修改时显示使用
- [x] 更加安全：密码记录文件所对应的账号，使用 BFM 账号进行 sha512 之后取希哈值。如此，就算得到密码的记录文件，也不知道原始账号，更别说还是加密的文件
- [ ] 更加安全：会主动探测密码的安全性，以及账号是否存在社工库信息，如密码不安全或账号不安全，会提示，（密码只分析强度，不做其他操作，账号会联网一些网站查询。如：[firefox](https://monitor.firefox.com/)）
- [ ] 更加安全：如果设置此账号仅自己一人知晓密码，会在本地配置文件目录生成此账号的登录记录，每次启动游戏或获取登录密码都会记录，之后会同官方后台的登录记录匹配。如发现没有记录在内，界面会变红色调，并提示
- [x] 更友好的操作体验：个性化登录页面，除星期三是固定背景图之外，其他时间都是随机背景图展示
- [x] 更友好的操作体验：账号列表不分港号、台号，用户直接选择记录的账号，就可以执行登录操作。
- [x] 更友好的操作体验：所有记录的账号信息，强制要求设置备注别名，以更直观知晓此账号是大号还是别人的号，又或者是工具号、仓库号等等
- [x] 更友好的操作体验：不同的账号状态，软件会自动创建对应状态的相关提示或功能
- [ ] 更友好的操作体验：锁号时，会自动查询原因，并提示解决方案
- [ ] 更友好的操作体验：出现 reCaptcha 时，会自动切换外部浏览器登录
- [ ] 更友好的操作体验：多处出现贴心提示，并会有长时间游戏，出现放松休息提示
- [ ] 还有很多，完成后再来补充

## 🏆 项目的开发人员

### 维护者

项目的维护者：

<a href="https://github.com/tikas"><img src="https://github.com/tikas.png" width="40" height="40" alt="tikas" title="tikas"/></a>

<details><summary>点我 打开/关闭 维护者列表</summary>

- [Tikas](https://github.com/tikas) - 项目作者，全能酱油王。

</details>

### 贡献者

特别感谢所有参与 TMS little helper 开发的贡献者。[贡献者列表](https://github.com/tikas/TMS-little-helper/graphs/contributors)

<a href="https://github.com/Loyisa"><img src="https://github.com/Loyisa.png" width="40" height="40" alt="Loyisa" title="Loyisa"/></a>

<details><summary>点我 打开/关闭 贡献者列表</summary>

- [Loyisa](https://github.com/Loyisa) - 技术大神，高尚的人格魅力，强大的技术能力，还 TM 的帅气！

</details>

## 🪄 如何构建

### 构建方法

本程序使用 aardio 开发，下载 aarido 最新版本( 仅 6.5MB，绿色免安装，永久免费 )

[https://ide.update.aardio.com/releases/aardio.7z](https://ide.update.aardio.com/releases/aardio.7z)

打开本项目，即可构建。

### 项目架构

```md
|—— .github                         Github 配置文件
| |—— ISSUE_TEMPLATE                Github Issue 模板
|—— DES                             DES 项目
|—— image                           项目展示图片
|—— main                            TMS little helper 项目
| |—— dlg                           窗口文件
|   |—— adduser.aardio              增加（修改）用户界面
|   |—— core.aardio                 核心主界面
|   |—— list.aardio                 用户列表界面
|   |—— qr.aardio                   QR 界面
| |—— lib                           用户相关库
|   |—— fonts                       字体图标文件夹
|   |—— config.aardio               项目配置文件
|   |—— listboxExx.aardio           用户列表自绘库
|   |—— perform.aardio              相关功能执行程序
|   |—— startGame.aardio            启动游戏前后相关的程序集
|   |—— tikas.aardio                一些核心加解密及初始值
| |—— res                           资源文件
|   |—— background                  登录程序的背景图片
|   |—— detect                      登录时 TSP 相关图片
|   |—— dll                         dll 文件
|     |—— lr144b1                   LR 转区 1.4.4-bate.1 版本
|   |—— img                         用户列表账号的缩略图
|   |—— start                       start 按钮相关图片
|   |—— welcome                     首次使用时的背景图片，图为本人，不得侵犯肖像权
|   |—— xtikas.ico                  Logo 图标
| |—— default.aproj                 aardio 项目文件
| |—— main.aardio                   TMS little helper 项目主入口
|—— CHANGELOG.md                    发布日志
|—— .gitignore                      git 排除项
|—— LICENSE                         许可证
|—— README.md                       中文 README
```

## 🪶 碎碎念

### 赞助

开发不易，觉得有很大帮助的朋友可以赏助(不接受学生赞赏)，以方便作者更有动力去开发。

### 开发背景

在现有的 [繽放 - 樂豆第三方客戶端](https://github.com/pungin/Beanfun) 还不支持港号新登录入口，而 [秋水橘子香港登入工具](https://github.com/starmcc/qs-beanfun) 又仅仅只支持港号登录，台号无法登录。

在提交了 [issues](https://github.com/pungin/Beanfun/issues/85) 想 Pungin 增加港号新登录入口时，却迟迟得不到下文，从这可以看出 Pungin 忙于其他事。

为此，只好重复造轮子了。

### 反馈

- 给开发者的反馈：[https ://github.com/Tikas/TMS-little-helper/issues](https://github.com/Tikas/TMS-little-helper/issues)
- 与其他用户讨论：[https://github.com/Tikas/TMS-little-helper/discussions](https://github.com/Tikas/TMS-little-helper/discussions)

>请不要在公开场合，透露个人信息（如账号、密码），因此导致损失，自行承担！

## 🖼️ 展示图

![display](https://raw.githubusercontent.com/Tikas/TMS-little-helper/main/image/display.webp)

## 💯 版权许可

[License MIT](../LICENSE)
