# hyperf-hex-admin
基于hyperf开发的后台权限管理系统
# 预览
+ [http://hyperf.26.do/admin/index.html](http://hyperf.26.do/admin/index.html)
+ 账号：`demo`
+ 密码：`123456`
+ 会话保持使用的`jwt`和`redis`，通过登录时间实现了`单一设备登录`，如果不需要限制单一设备登录，找到Auth中间件删除对应的逻辑代码即可
# 安装
`composer install `
# 导入数据库
`hex.sql`
# 运行
`php bin/hyperf.php start`
# 访问后台
+ 网址：`http://127.0.0.1:9501/admin/index.html`
+ 账号：`admin`
+ 密码：`123456`
# 优势
+ 基于layui前后端分离开发，页面占内存超低，再也不用怕被老板说卡的半死了
+ 代码清晰，扩展简单
+ 字典管理，一目了然
+ 前端界面无需写一行代码，可以实现自动生成`复杂新增`,`复杂修改`,`复杂查询`,`批量删除`
+ 由于时间原因，前端自动生成代码的文档还没写，但是所有的代码逻辑已经实现，完全基于字典数据实现，自动读表和读字典进行界面渲染
+ 字典数据是什么？就是无论你想在`增、改、查`的时候任何地方，你都可以不用写代码，直接复制粘贴（后面会实现自动生成代码），就可以实现你想要的功能。
+ 想了解功能直接看前端代码（`public/admin/module/src/views`）以及控制器代码，这些代码你都可以直接复制粘贴直接使用
# 依赖
+ redis扩展（其实根本没用到，因为hyperf在注入协程redis的时候需要用到`\Redis`，所以需要安装扩展）
+ swoole4.4（hyperf就是基于这个强大的协程框架开发的，所以我们必须要安装她）
# 遇到的问题
由于我是基于php7.4开发，所以语法全是php7.4的语法，务必使用php7.4跑，但是`composer install`的时候会出现报错，所以你可以使用php7.2的`composer install`进行安装，如果报依赖php版本错误，请修改`composer.json`里面的php版本依赖为7.2即可，等待安装完成后，在切换到php7.4环境下进行运行
# 后期技术支持
+ 本后台框架以及文档会持续更新
+ 后期会实现不写一行代码，直接自动生成界面
+ QQ群：423317994
+ 暂时没文档，有什么问题直接问群主
