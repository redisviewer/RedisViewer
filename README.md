### 介绍
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/00e2edc6-9ca3-48f5-9d7b-a0e38b07e380" />

1.  RedisViewer为一款追求极致性能、低内存占用、极简布局、高效交互、跨平台、支持反序列化Java字节码的redis桌面客户端。
2.  经测试局域内网环境连接200万key不到两秒。本地已验证5000万key数据量redis服务器流畅使用，且内存占用同比偏低。
3.  渲染性能不受数据量影响：大数据量情况下部分同类软件可能遇到性能瓶颈崩溃或内存暴涨，RedisViewer拥有经历多次重构迭代的虚拟显示技术，针对rv的数据流特征深度调优，力保渲染交互流畅。
4.  解决研发、测试、运维工作中使用redis可视化工具的痛点问题，功能范围尽力覆盖所有redis使用角色。
5.  有任何建议可以评论区留言或发送邮件<124410675@qq.com>

<!---->

    支持Windows、MacOS、Linux，方便不同平台开发者们使用！ 
    系统版本要求：
        macos >= 10.14.x
        windows >= 8
        linux 未验证

### 下载地址：

[RedisViewer3下载](https://www.123865.com/s/Sxw9-jU4bv)

### 大数据列表

RedisViewer构思阶段的第一个要解决的问题就是大量数据的展示渲染。也是该软件的核心功能，其多个组件在用：key列表、list/set/zset/hash编辑器

针对大数据量优化：迭代调整了多个渲染方案，解决同类软件渲染时内存占用痛点。实测可见前100万数据，行高33px达到浏览器高度上限33554432px，剩余数据可通过关键字快速过滤出来，作者也在寻找完美显示方案，欢迎网友讨论

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/da64b24f-f22a-4148-8d37-55f1fea3087d" />




### 支持结构化搜索

支持结构化搜索：自动分析key拆分结构化，redis库里都存了什么key一目了然（大数据列表高度上限只能显示100万的补偿搜索方案）

另外支持搜索历史记录、检索

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/69100479-70dc-4dd7-a62c-1407594ca043" />




### Java反序列化查看器

Java字节码反序列化解码展示，全网唯一 ，终于知道老项目redis存了个啥。 不仅看得到还要合理好看

支持数据结构：基础类型、包装类型、一维数组、ArrayList、LinkedList、HashMap、HashSet、Date、Time、TimeStamp等等

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/4fa2c631-976e-4e1b-bf2e-1c8c7d886167" />




### 高性能编辑器

专业高性能编辑器，实时语法提示、语法检查

支持超多语言，redis里面存代码也能读了

### JSON、XML自动格式化

string、xml类型的数据：展示时如果是JSON格式则将自动格式化方便阅读，保存时会进行JSON格式再校验、压缩、提交

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/bd606527-fb6f-46b5-bef0-cabfacf81a6a" />
沉浸式编辑器

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/8c4bc7b1-c232-4af3-94fa-1906d18dd88b" />


沉浸式编辑器

### 归类分组

常见使用树形来展示归类分组，大数据量情况下的树形将会卡爆，深有体会的小伙伴儿应该蛮多的吧

软件使用了页签导航的展现形式，另辟蹊径的解决大数据量分组树形的渲染问题

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/74e74550-80ec-4cd0-b112-79b30c25aeb9" />




### 沉浸式控制台

支持命令详情提示的控制台、支持集群redis节点切换、命令分块折叠。支持不拉取数据连接到redis服务器使用命令行，省去ssh登录到服务器上面敲redis-cli命令的繁琐过程

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/6db51727-282f-4b18-8b73-df0c789f186f" />


沉浸式控制台

### 导入导出

开发人员最想干什么？当然是把现网（或另一环境）的数据导入到本地快速定位问题。特别推出导入导出功能，可谓是研发利器

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/d78856ec-c3e5-4aca-860e-12201ad63fb3" />


输入图片说明

### 支持SSH：单机&集群

同时支持单机与集群的SSH ，不少类似软件的支持度也相对欠缺。

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/2fbb87cd-db88-4ae7-8d8a-420f3800f0ed" />




### 极速索引

关键字极速过滤（内存），相比同类软件更便捷、更快的索引数据

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/9d1b925e-e884-4d7f-9ab2-2fc983af73e8" />



### 设置页面
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/b4e595d2-cb82-4e54-ba94-2741baad171c" />


### 安装教程

下载Redis Viewer-xxx安装包，运行就可以安装Redis Viewer。

    Windows --> Redis Viewer-win-2.4.2.exe
    MacOS --> Redis Viewer-mac-2.4.2.dmg
    Linux --> Redis Viewer--linux-2.4.2.deb
        Debian系: .deb
        Arch系: .pacman
        红帽系: .rpm
        通用: .AppImage .zip 


其他类似软件

之前介绍过几款类似的工具，他们分别是RedisView、WebRedisManager、RedisDesktopManager、RedisPlus、AnotherRedisDesktopManager等，也基本满足了开发者的需求，也都会有不足之处，感兴趣的小伙伴们可以自行搜索或者好看笔者以往的文章，此处不再详细介绍！

![](https://p0-xtjj-private.juejin.cn/tos-cn-i-73owjymdk6/1da3e6e6f2f640dc8bc7ccb53ba720fc~tplv-73owjymdk6-jj-mark-v1:0:0:0:0:5o6Y6YeR5oqA5pyv56S-5Yy6IEAgUmVkaXNWaWV3ZXI=:q75.awebp?policy=eyJ2bSI6MywidWlkIjoiMTgyMDQ0Njk4NzEyNjc0OSJ9&rk3s=f64ab15b&x-orig-authkey=f32326d3454f2ac7e96d3d06cdbb035152127018&x-orig-expires=1735192115&x-orig-sign=Ho90JR2DhTzWpSCPLS%2B3EtwkSAU%3D)



## 总结

好用的软件千千万，好用的Redis客户端管理软件可真不多，本文向大家介绍了这样一款综合其他同类软件优点，又扩展了一些特色功能的RedisViewer，如果你有类似的需求不妨尝试下这款工具，或许能带给你一些惊喜！

### 下载地址：

[RedisViewer3下载](https://www.123865.com/s/Sxw9-jU4bv)

#### 请作者喝咖啡
<img src="https://foruda.gitee.com/images/1662602721400259841/0f2c822e_968935.png" alt="drawing" width="260"/>
