# ezg-wx.woa
亿账柜woa系统微信小程序扩展

## 说明

工程项目由gulp构建，需要node环境。
因为小程序官方工具带有代码压缩和ES6转换功能，所以这部分功能由小程序官方工具实现，保留官方工具的调试功能。
gulp中使用了大量开源插件，对此表示感谢。

## 演示
这里在官方模拟器上演示服务审批权限的功能，部分不能使用的功能类似。
### 截图：
![首页](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/index.png)

![工作](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/works.png)

![应用](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/application.png)

![列表](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/list.png)

![搜索](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/search.png)

![详情](https://github.com/zwei76/ezg-wx.woa/raw/master/screenshots/detail.png)

### 视频演示
[演示视频地址](http://yuntv.letv.com/bcloud.html?uu=rz15dixzpg&vu=1ce67345e2&pu=31d219913c&auto_play=1&width=640&height=480&lang=zh_CN)

## 目录结构

 - src为开发目录；
 - dist为部署目录；
 - gulpfile.js为gulp配置；
 - package.json为整个工程的配置信息。

## 使用说明（gulp操作）

0. 安装依赖，运行npm install；
1. 默认命令，将监视src文件变化自动构建项目到dist；
2. 构建项目
 - build:all  （构建整个项目，就是下面这些的合集，并且复制了其它文件）
 - build:style  （处理样式表）
 - build:images  （图片压缩）
3. 复制不需要处理的文件
 - copy:all  （复制全部其它文件，就行下面这些的合集）
 - copy:main  （复制根目录文件，即app.json和app.js）
 - copy:pages  （复制页面文件）
 - copy:templates  （复制模板文件）
 - copy:utils  （复制工具类文件）
4. 清除图片缓存（为了避免重复压缩图片太过费时，使用了缓存，但如果修改了图片就可能要清除缓存）
 - clean:cache
5. 清理部署目录（会将dist目录的所有东西清除）
 - clean:all
6. 打包压缩
 - zip  （会先执行clean:all，再执行build:all，最后压缩dist目录生成一个由日期命名的压缩包）

## 架构设计
[原型地址](http://xa01e4.axshare.com)  

## todo
1. 完善工作页面；
2. 搜索和筛选的功能；
