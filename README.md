### 介绍

1.  RedisViewer为一款追求极致性能（海量数据下低内存占用）、极简布局、高效交互、跨平台、支持反序列化Java字节码的redis可视化客户端工具。
1.  软件运行机制：(1)拉取key，(2)内存排序，(3)分组归纳，(4)异步结构索引分析。局域内网环境测试200万key不到两秒。
1.  本地已验证5000万key数据量redis服务器流畅使用，且内存占用低。
1.  渲染性能：大数据量(1万+)情况下同类软件由于渲染问题可能已经崩了，RedisViewer拥有经历多次重构迭代的虚拟显示技术，针对rv的数据流特征进行调优，交互性能优秀不受数据量的影响。
1.  WEB技术客户端美观，能够支持、实现的交互方式更丰富
1.  进化方向：解决研发、测试、运维工作中使用redis可视化工具的痛点问题。功能不是最多的，但关键功能经历多次进化深耕，体验有保证。
1.  兴趣主导的项目，进度随性。该软件并不适合所有人，使用时请斟酌自行判断。
1.  有任何建议可以评论区留言或发送邮件124410675@qq.com

支持Windows、MacOS、Linux，方便不同平台开发者们使用！
```
系统版本要求：
    macos >= 10.14.x
    windows >= 10
    linux 未验证
```
<img width="1280" alt="图片" src="https://github.com/user-attachments/assets/8fd24a2a-d5b8-4ce8-a5b0-21bd154b7acf">

添加图片注释，不超过 140 字（可选）

### 下载地址：
[RedisViewer下载: https://www.123pan.com/s/Sxw9-WiAbv.html](https://www.123865.com/s/Sxw9-jU4bv))


### 后端重构

使用Golang语言重构核心代码

启动快、内存低，且实时自动伸缩

### 大数据列表

RedisViewer构思阶段的第一个要解决的问题就是大量数据的展示渲染。也是该软件的核心功能，其多个组件在用：key列表、list/set/zset/hash编辑器，控制台

针对大数据量做了优化：迭代调整了多个渲染方案，解决同类软件渲染时内存占用痛点。实测可见前100万数据，行高33px达到浏览器高度上限33554432px，剩余数据可通过关键字快速过滤出来，作者也在寻找完美显示方案，欢迎网友讨论

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/3e7e7458413447d7b6349dc650017155~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=69742&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### 支持结构化搜索

支持结构化搜索：自动分析key拆分结构化，redis库里都存了什么key一目了然（解决大数据列表高度上限只能显示100万的疑难问题，算是一个补偿方案）

另外支持搜索历史记录、检索

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/680deab6d5174f2f8069899396b234b5~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=48139&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### Java反序列化查看器

Java字节码反序列化解码展示，全网唯一 ，终于知道老项目redis存了个啥。 不仅看得到还要合理好看

支持数据结构：基础类型、包装类型、一维数组、ArrayList、LinkedList、HashMap、HashSet、Date、Time、TimeStamp等等

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a58802b3c02b48099f057184fc624650~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=73000&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### JSON编辑器

专业编辑器，实时语法提示、语法检查

支持超多语言，redis里面存代码也能读了

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6b46b27471d243da838a5fef72dbcae8~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=97478&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/af54b3e6c5154a5f85fdf2b31b06ec9c~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=66869&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### 归类分组

常见使用树形来展示归类分组，大数据量情况下的树形将会卡爆，深有体会的小伙伴儿应该蛮多的吧

软件使用了页签导航的展现形式，充分发挥大数据列表的优势，算是另辟蹊径的解决大数据量分组树形的渲染问题

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/c73dfa2c5c054ceeabf73a75b781735b~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=60034&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### 控制台

支持「直接模式」命令的控制台，同时支持目标节点切换，再也不用ssh登录到服务器上面敲命令了

MOVED自动跳到目标节点执行

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8fe89078603941cbab85d3afb090f0ec~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=113175&e=png&b=3c3f41)

添加图片注释，不超过 140 字（可选）

### 导入导出

开发人员最想干什么？当然是把现网（或另一环境）的数据导入到本地快速定位问题。特别推出导入导出功能，可谓是研发利器

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/7849a355502547d78ae99d8ca940cec8~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=444&s=73430&e=png&b=fcfcfc)

输入图片说明

### 支持SSH：单机&集群

同时支持单机与集群的SSH ，不少类似软件的支持度也相对欠缺。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f15c30303c914243a4cf2c37285700e1~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=44792&e=png&b=fcfcfc)

添加图片注释，不超过 140 字（可选）

### JSON自动格式化展示

string类型的数据：展示时如果是JSON格式则将自动格式化方便阅读，保存时会进行JSON格式再校验、压缩、提交

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ffc19d19b2b1466987df21ec8f270cc6~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=423&s=128832&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

### 极速索引

关键字极速过滤（内存），相比同类软件更便捷、更快的索引数据

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b46aa927d1a44e25b36b4235229b7580~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=444&s=27582&e=jpg&b=fcfcfc)

输入图片说明

### 软件架构

```
Electron 28.x
Golang 1.22.x
```

### 安装教程

下载Redis Viewer-xxx安装包，运行就可以安装Redis Viewer。

```
Windows --> Redis Viewer-win-2.4.2.exe
MacOS --> Redis Viewer-mac-2.4.2.dmg
Linux --> Redis Viewer--linux-2.4.2.deb
    Debian系: .deb
    Arch系: .pacman
    红帽系: .rpm
    通用: .AppImage .zip 
```

### 使用说明

### 1. 远程模式

> 访问非局域网redis服务器时，10万以上大数据量key的获取时间成倍增加... 主要瓶颈可能是服务器的上行带宽。

远程模式即远程接力模式，程序将直接访问远端RedisViewer进行网络接力，屏蔽高延迟网络差异，获得极速访问redis服务器的能力。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/03ea1ea0d5f64e1f83b95ab87e1a6df7~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=746&h=352&s=20306&e=png&b=fdfdfd)

添加图片注释，不超过 140 字（可选）

带来的好处是：即使居家办公或redis服务器部署在公网，也能够以极高的网络速度访问、获取数据量比较多的redis服务器（远程RedisViewer需要跟redis服务器是局域网，二者网络通信效率要高）。

### 1.1 远程服务器要打开RedisViewer（若远程为无界面的server系统，则需要执行./redismanager -conf configs这里需要提取目标系统版本的相关文件自己部署，对动手能力有一定的要求）。

### 1.2 设置页面配置远程地址

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/35af056b8a51446b8d3ad660d3ddfc71~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=450&s=81235&e=png&b=fefefe)

添加图片注释，不超过 140 字（可选）

### 1.3 切换配置的远程

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/576d3dca9cb64dd2b17930d7092e252c~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=444&s=21718&e=jpg&b=fdfdfd)

远程切换

### 注意：

远程RedisViewer跟Redis服务器二者网络效率要高，必须是局域内网。

10万以上数据量key的reids服务器，由于拉取key数量较大，建议使用远程模式享受远程的高性能网络（适用居家办公），10万以下本地依然效率很高

### 2. SSH隧道

本质上就是端口转发。它能够将其他 TCP 端口的网络数据通过 SSH 链接来转发，并且自动提供了相应的加密及解密服务。这一过程也被叫做“隧道”（tunneling），这是因为 SSH 为其他 TCP 链接提供了一个安全的通道来进行传输而得名。 SSH 端口转发能够提供两大功能： 1.加密 SSH Client 端至 SSH Server 端之间的通讯数据。 2.突破防火墙的限制完成一些之前无法建立的 TCP 连接。

### 开启SSH隧道并正确填写

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e851266da2cc40b7b79ff7857e746acc~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=43951&e=png&b=fefefe)

添加图片注释，不超过 140 字（可选）

### 反馈通道

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b3846da456944e338f8313f937bdc584~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=720&h=432&s=50137&e=png&b=fcfcfc)

添加图片注释，不超过 140 字（可选）

其他类似软件

之前介绍过几款类似的工具，他们分别是RedisView、WebRedisManager、RedisDesktopManager、RedisPlus、AnotherRedisDesktopManager等，也基本满足了开发者的需求，也都会有不足之处，感兴趣的小伙伴们可以自行搜索或者好看笔者以往的文章，此处不再详细介绍！

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a516bc99560948a0b745912303445d3f~tplv-k3u1fbpfcp-jj-mark:0:0:0:0:q75.image#?w=640&h=360&s=40444&e=jpg&b=e2e1e1)

添加图片注释，不超过 140 字（可选）

## 总结
好用的软件千千万，好用的Redis客户端管理软件可真不多，本文向大家介绍了这样一款综合其他同类软件优点，又扩展了一些特色功能的RedisViewer，如果你有类似的需求不妨尝试下这款工具，或许能带给你一些惊喜！

### 下载地址：
[RedisViewer下载: https://www.123pan.com/s/Sxw9-WiAbv.html](https://www.123865.com/s/Sxw9-jU4bv))


注意：1.4、1.5版本升级2.x版本，需要先删除用户目录下.redis_viewer文件夹，例如：
> C:\Users\Administrator\.redis_viewer /home/zhang3/.redis_viewer

#### 请作者喝咖啡
<img src="https://foruda.gitee.com/images/1662602721400259841/0f2c822e_968935.png" alt="drawing" width="260"/>
