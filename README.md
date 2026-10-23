# WebSys
学着微博写的 Web 小项目，**ASP.NET WebForms + SQL Server**。发帖、看信息流这类微博的基本功能都葫芦画瓢写了一遍。

```
浏览器 ──► IIS Express ──► WebForms 页面（WebApplication1/）──► SQL Server
```

## 快速开始

### 1. 打开项目
用 Visual Studio 打开 `WebApplication1/` 下的项目文件（VS2019 起步，别用太老的版本）。

### 2. 建数据库
仓库里没放 SQL 脚本，自己建一个空库，然后把 `Web.config` 里的连接字符串改成你的：

```xml
<connectionStrings>
  <add name="WebSys" connectionString="Data Source=.;Initial Catalog=WebSys;Integrated Security=True" />
</connectionStrings>
```

> 连接串叫什么名字以 `Web.config` 里实际写的为准，别照抄上面这段。

### 3. 跑起来
F5 起 IIS Express，浏览器会自己弹首页。Windows 防火墙弹窗的话选「允许」。

## 目录

```
WebSys/
├─ WebApplication1/   # 网站主体：页面和后台代码
├─ Modles/            # 实体类（目录名拼错了，将就看）
├─ css/ fonts/ img/   # 静态资源
└─ README.md
```

## 常见问题

- **打不开，报连不上数据库**：九成是连接字符串没改，或者本机 SQL Server 没启动。
- **样式全是乱的**：css、字体都是相对路径，必须从站点根目录访问，别把单个 `.aspx` 抠出来直接双击打开。
- **代码风格很野**：对的，新手期写的，能跑就行。

