### 调试插件vue-devtools安装

插件官网：[https://github.com/vuejs/vue-devtools](https://github.com/vuejs/vue-devtools)

安装步骤：

#### 第一步：clone或者下载zip

> 建议直接从github上下载zip，然后解压
>
> clone方式：

```
先在本地创建一个文件夹：比如vue或者其他【clone的时候会自动生成vue-devtools文件夹】
进入该文件夹，shift+右键，选择“在此处打开命令窗口”

将github上的项目克隆到本地：git clone https://github.com/vuejs/vue-devtools.git
会自动生成vue-devtools文件夹，clone速度会比较慢，建议下载zip，然后解压
```

#### 第二步：安装项目依赖

在安装过程中，会存在权限，网络等问题导致安装失败

安装步骤一：

> 强烈建议：以管理员身份运行cmd，使用国内源进行安装：npm install --registry=[https://registry.npm.taobao.org](https://registry.npm.taobao.org)

执行以上命令后，可能会报错：原因应该是网络问题导致某些包下载不到

![](/assets/import.png)

解决办法如下，可以参考：[issues](https://github.com/vuejs/vue-router/issues/261#issuecomment-218618180)

> npm install --chromedriver\_cdnurl=[http://cdn.npm.taobao.org/dist/chromedriver](http://cdn.npm.taobao.org/dist/chromedriver)

执行chromedriver命令后，又可能会报错如下：缓存导致的报错

> 解决办法：npm cache clean --force

![](/assets/import1.png)

执行完npm cache clean --force，再执行npm install --chromedriver\_cdnurl=[http://cdn.npm.taobao.org/dist/chromedriver，](http://cdn.npm.taobao.org/dist/chromedriver，)

不出意外应该就能正常下载了

![](/assets/import2.png)

第三步：编译项目文件

> npm run build

第四步：添加到chrome浏览器

```
1. 在浏览器地址栏中输入 chrome://extensions/
2. 勾选开发者模式
3. 加载已解压的扩展程序：选择vue-devtools\shells目录下的chrome
```

![](/assets/import3.png)

