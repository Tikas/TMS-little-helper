<p align="center">
    <h3 align="center">TMS little helper</h3>
    <p align="center">一个致力于 TMS (TW MapleStory) 更好的启动、登录、多账号管理等相关解决方案。</p>
</p>

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

### 国际化

README：~~English~~ | 中文

### 项目介绍

TMS小帮手，一个致力于 TMS (TW MapleStory) 启动、登录、多账号管理等相关的小程序。

![display](https://raw.githubusercontent.com/Tikas/TMS-little-helper/main/image/display.webp)

### 开发背景

在现有的 [繽放 - 樂豆第三方客戶端](https://github.com/pungin/Beanfun) 不支持港号新登录入口，而 [秋水橘子香港登入工具](https://github.com/starmcc/qs-beanfun) 又仅支持港号登录。

他们都有个共同点：依赖运行库。

在提交了 [issues](https://github.com/pungin/Beanfun/issues/85) 想 pungin 增加港号新登录入口时，却迟迟得不到下文，从这可以看出 pungin 一定忙于其他事。

为此，只好重复造轮子了。

### 功能特色

- ~~去运行库~~：由于 DES 解密使用了 pungin 的代码，使用 .Net 核心 CLR 调用，理论上，只要有 .Net 运行库就能执行。win 10 + 无需要进行额外设置，win 7 用户建议安装 ,Net 4.0+ 以上的版本即可。
- 更友好体验：尽可能做到发生一些情况时，能主动出现原因或解决方法，而不用去询问网络或他人。
- 更安全：增加许多安全功能，以提高安全性。
- ~~更多实用功能~~：目前还处于基础功能开发状态，这个后续再加。

### 维护者

项目的维护者：

<a href="https://github.com/tikas"><img src="https://github.com/tikas.png" width="40" height="40" alt="tikas" title="tikas"/></a>

<details><summary>点我 打开/关闭 维护者列表</summary>

- [tikas](https://github.com/tikas) - 项目作者，全能酱油王。

</details>

### 贡献者

特别感谢所有参与 TMS little helper 开发的贡献者。[贡献者列表](https://github.com/tikas/TMS-little-helper/graphs/contributors)

<a href="https://github.com/Loyisa"><img src="https://github.com/Loyisa.png" width="40" height="40" alt="Loyisa" title="Loyisa"/></a>

### 架构

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
|   |—— tikas.aardio                一些核心加解密及初始值
|   |—— web.aardio                  弃用：还没写好的网络请求功能
| |—— res                           资源文件
|   |—— background                  登录程序的背景图片
|   |—— detect                      登录时 TSP 相关图片
|   |—— dll                         dll 文件
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

### 如何构建

本程序使用 aardio 开发，[下载 aarido 最新版本( 仅 6.5MB，绿色免安装，永久免费 )](https://ide.update.aardio.com/releases/aardio.7z)，打开本项目，即可构建。

### 赞助

开发不易，觉得有很大帮助的朋友可以赏助(不接受学生赞赏)，以方便作者更有动力去开发。

### 版权许可

[License MIT](../LICENSE)
