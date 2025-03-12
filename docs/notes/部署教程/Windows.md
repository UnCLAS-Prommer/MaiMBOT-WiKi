---
title: Windows部署
permalink: /deploy/windows/
createTime: 2025/03/12 15:31:15
---
## 一：安装Python环境

### 下载[安装包 ](https://www.python.org/downloads/)                

<img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMKZ8saxfRoWJCPzj1nmdMVH7vH3eEAAtfGMRuICVlW1Gyk0xzvFHsBAAMCAAN3AAM2BA.png" alt="image-20250307230039422" style="zoom: 67%;" />

单机黄色按钮下载安装包

### 安装过程 

<img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMMZ8scf6pzzT58hSC1-SUXYr9uAdsAAubGMRuICVlWxkloUeFlWnEBAAMCAAN4AAM2BA.png" alt="Python安装界面" style="zoom:67%;" />  

✅ 必须勾选 `Add Python.exe to PATH`  
🔘 选择 `Install Now` 完成安装

## 二：部署MongoDB数据库

### 获取安装包

[MongoDB官方下载](https://www.mongodb.com/try/download/community/)  *推荐使用IDM等下载工具加速*

<img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMVZ81MOfGDue3rMgh-bbmM_f6bCu8AAmXJMRsDfGhWkGyyg5tnATwBAAMCAAN3AAM2BA.png" style="zoom: 25%;" />

> - MongoDB 的版本偶数版本为稳定版，奇数版本为开发版。
>
> - MongoDB 对于32位系统的支持不佳，所以3.2版本之后就没有对32位系统的支持。
>
> - **MongoDB for Windows 64-bit** 适合 64 位的 Windows Server 2008 R2, Windows 7 , 及最新版本的 Window 系统。
>
> - **MongoDB for Windows 64-bit Legacy** 适合 64 位的 Windows Vista, Windows Server 2003, 及 Windows Server 2008 。
>
> - **MongoDB for Windows 32-bit** 适合 32 位的 Window 系统及最新的 Windows Vista。 32 位系统上 MongoDB 的数据库最大为 2GB。
>
> 
>
>   下载 **.msi** 文件，下载后双击该文件，按操作提示安装即可。

### 安装过程

双击打开安装包：                                       

![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMJZ8sauA6a0rNHXOhYZORUnCVMeXgAAtbGMRuICVlWUz_BJiUCVq4BAAMCAAN4AAM2BA.png)

接下来，将出现一个协议窗口，选中同意的选项，然后再点击 "Next" 按钮：

![img](https://www.runoob.com/wp-content/uploads/2013/10/image2-5.png)

此时出现两个选项：

- `Complete` *完整安装*  **默认配置安装所有 MongoDB 组件和工具，当然你也可以选择自定义安装。**
- `Custom` 自定义安装

![img](https://www.runoob.com/wp-content/uploads/2013/10/Steps-to-install-MongoDB_4.png)



*一般选择完整安装即可*

<details>
  <summary>点击展开</summary>


自定义安装会多出如下选项，你可以自定义MongoDB本体安装路径以及可选组件

![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMtZ9BhOo2uM8xivleEMPjRKOa9Zj4AAgvAMRsN34BWwOjNF9fSYAEBAAMCAAN4AAM2BA.png)

</details>

  现在，出现了两个选择：

   ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMnZ814HfaBlaf3EzVrZCJsJEJ6InYAAgbKMRsDfGhWY7YWSY8_FW0BAAMCAAN4AAM2BA.png)

> 从**MongoDB 4.0**开始，您可以在安装期间配置和启动**MongoDB**作为服务，并在成功安装后启动**MongoDB**服务
>
> - **Run Service as Network Service user**：以网络服务用户身份运行服务（默认）
>
>  - 这是Windows内置的Windows用户账户
>
> - **Run Services as a local or domain user**：以本地或域用户身份运行服务对于现有本地用户账户
>
>  - Domain填"."(小数点)即可
>  - Account Name为当前Windows用户名
>  - Account Password为Windows用户密码 ==（注意不是PIN密码）==
>  - 对于现有的本地用户帐户，请指定一个句点作为帐户域（即.），并为该用户指定帐户名称和帐户密码。
>  - 对于现有域用户，请为该用户指定“ 帐户域”，“帐户名”和“ 帐户密码 ”
>
>   **如果您只需简单操作和基本功能，默认的网络服务用户选项即可**
>   **如果您需要对权限进行更多控制，或者需要使用特定用户凭据访问和限制资源，则选择本地或域用户选项会更合适**
>
> - Service Name：指定服务名称，默认名称是MongoDB。如果您已拥有具有指定名称的服务，则必须选择另一个名称
>
> - Data Directory：指定数据目录，对应于–dbpath。如果该目录不存在，安装程序将创建该目录并设置对服务用户的目录访问权限
>
> - Log Directory：指定日志目录，该目录对应于–logpath。如果该目录不存在，安装程序将创建该目录并设置对服务用户的目录访问权限
>
> - 只安装MongoDB（不推荐）

这里我们可以直接`next`:

**Install MongoDB Compass：**

安装**MongoDB**的**GUI**软件，因为网络的原因,某些地区可能下载很慢，如果您遇到这种情况，请尝试去掉勾选，可在安装完成之后另外[下载安装](https://www.mongodb.com/try/download/compass)。

![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMpZ814g7k-7leb3NiByYBh4i5zmYcAAn7EMRsDfHBWVLP095keYsoBAAMCAAN4AAM2BA.png)

   ***至此，MongoDB安装完成了✅***
   安装完毕之后，默认会自动运行数据库服务。浏览器打开 [此链接](http://localhost:27017/) 出现以下文字表明数据库正在运行！

   > It looks like you are trying to access MongoDB over HTTP on the native driver port.

   *您可以通过修改MongoDB的`bin`目录下的`mongod.cfg`来修改服务运行配置*

启动 MongoDB 服务

``` cmd
net start MongoDB
```

关闭 MongoDB 服务

``` cmd
net stop MongoDB
```

移除 MongoDB 服务

``` cmd
mongod --remove
```

### 添加环境变量 (还是指令大佬)

如果您不想用MongoDB Compass对数据库进行管理，也不想使用MongoDB自带的shell工具，而是想在Windows CMD/PowerShell中执行命令，那您还需要多一步**添加环境变量**:

只需摁住Win+R打开运行窗口输入: 

```cmd
setx path "%path%;MongoDB的bin路径" /M
```

例如我的MongoDB的`bin`路径为`C:\Program Files\MongoDB\Server\8.0\bin`，那么我只需要输入

```cmd
setx path "%path%;C:\Program Files\MongoDB\Server\8.0\bin" /M
```

:::warning

只能用运行窗口或CMD运行该命令

严禁使用PowerShell运行该命令

严格按照要求输入命令

打错出事别来找我

:::

## 三：配置NapCatQQ框架

### 下载安装

[NapCatQQ最新版](https://github.com/NapNeko/NapCatQQ/releases/)  
选择 `Win64无头版本（网盘链接）`或`NapCat.Shell(GitHub发行直链)`

![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMWZ81avJxQRdCjP1TyQVO3izHWNAkAAqbJMRsDfGhWbxC3eJfrGyQBAAMCAAN3AAM2BA.png)

在你喜欢的地方新建一个文件夹命名为NapCat.Shell，将下载下来的压缩包解压到此处

### NapCat,启动！

1. *强迫症*必须重命名`quickLoginExample.bat`为`quickLogin.bat`，接着右键编辑， ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMXZ81dfs2aDVi1PuNE4iin76klQfwAAq_JMRsDfGhWYzu3goS3WZMBAAMCAAN4AAM2BA.png)

   ==带有`REM`的为注释 删掉*你需要的系统*的那行命令开头REM这三个单词，并把`123456`修改为你*需要自动登录的Bot的QQ号*=={.important}

2. **保存（Ctr+S）**退出并运行该脚本即可启动**NapCat.Shell**

   如图，在启动后会出现一行`[NapCat] [WebUi] WebUi Local Panel Url: http://127.0.0.1:端口号/webui?token=密码`

   摁住Ctrl键并单击链接即可跳转到浏览器打开*NapCat*的**WebUI**

   ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMuZ9EWbZlsk0ZWSY2-CdMSF73DKi8AA8UxGw3fiFY7idYss2Gj6wEAAwIAA3kAAzYE.png)

   按照提示进行登录后即可进入管理界面

   ### 配置WebSocket客户端

   此时点击左侧边栏的`网络配置`菜单：

   ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMvZ9EYCbJhx5m0yqq_9ttoS1rBWocAAgvFMRsN34hWuCnC18_1y2ABAAMCAAN3AAM2BA.png)

   鼠标移到`新建`选项上，点击`Websocket`客户端

   ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMwZ9EZhey6BOrGTXQxaeTVtgIxj-8AAhXFMRsN34hW6WKs-qq_GsMBAAMCAAN3AAM2BA.png)

随后在弹出的窗口

单击`启用`

`名称`起一个你想要的名字，比如我填的是`MaiMBOT`

**`URL`**填入`ws://127.0.0.1:8080/onebot/v11/ws`

**`消息格式`**选择*`String`*字符串格式

其余保持默认即可，点击**`保存`**

![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMxZ9EZ9UXUQXry2cpC00xjjNZYn_kAAhjFMRsN34hWXlegBnNg0nkBAAMCAAN4AAM2BA.png)

恭喜你配置完了***NapCatShell***🥳

## 四：获取MaiMBot主体

如果无法访问到Github请尝试使用[Steam++](https://steampp.net/)，软件使用[教程](/tool/visit-git/)

**GitHub获取**  
访问项目[仓库](https://github.com/SengokuCola/MaiMBot)，切换到debug分支下

<img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMjZ81pvYSeUaeKcmlhfBelH_GlNa8AAuzJMRsDfGhWCX4ePAdy7noBAAMCAAN5AAM2BA.png" style="zoom: 67%;" />

接着点击绿色的`Code`按钮，点击`Downlod ZIP`下载压缩包

<img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMiZ81psAdqhyPbuSfeQOBTPMf90jsAAurJMRsDfGhWvQgVmBjrQdgBAAMCAAN5AAM2BA.png" style="zoom: 67%;" />



将压缩包解压到你喜欢的地方

## 五：申请API密钥

### SiliconCloud

1. **注册**  (包含我的邀请链接，注册赠送14元余额)
   [注册入口](https://cloud.siliconflow.cn/i/Dp1gWkNo)

2. **创建密钥**  
   <img src="https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMgZ81oCKbZp5zApcY2IN2CtpHGcFUAAufJMRsDfGhWhzj-SoSP7owBAAMCAAN3AAM2BA.png" style="zoom: 50%;" />
   点击右上角 `新建API秘钥` 生成密钥,弹出的窗口直接点击`新建密钥`，描述可以不填，创建完成后单击密钥文本即可复制下来

   ![](https://zip-image.pages.dev/file/AgACAgUAAyEGAASIL8CVAAMhZ81oudpTENp46Ll3_P7PR2DcGZ0AAunJMRsDfGhWH-GbWH9SXdUBAAMCAAN4AAM2BA.png)

## 六：项目环境配置

### 打开终端

打开你之前从GitHub上下载并解压缩的MaiMBot-debug文件夹，找一处空白的地方，右键`在终端中打开(T)`

### 创建虚拟环境 (如果你不知道虚拟环境是什么，那请  跳过此步骤)

```powershell
python -m venv bot
bot\Scripts\activate 
```

### 配置清华镜像源

```powershell
pip config set global.index-url https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple
pip install -r requirements.txt
```

### 初始化项目

在shell/cmd输入以下命令后再关闭

```powershell
nb run
```


## 📎 资源汇总    

| [Python官网](https://www.python.org/downloads/)              |
| ------------------------------------------------------------ |
| [(Steam++)Watt Toolkit官网](https://steampp.net/)            |
| [NapCatQQ仓库](https://github.com/NapNeko/NapCatQQ/releases/) |
| [MaiMBot仓库](https://github.com/SengokuCola/MaiMBot/tree/debug) |
| [MongoDB下载 ](https://www.mongodb.com/try/download/community/) |
