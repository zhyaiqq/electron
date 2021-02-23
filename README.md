## vue3和electron搭建开发桌面应用环境
之前从没有了解过electron，发现有些招聘要求有需求，就准备学习一下electron,看了官方的一些文档基本有了了解，然后一想我们开发都是基于vue或者react,所以这里记录了在vue3中搭建electron环境的过程。

首先初始化一个vue3项目，然后新建`vue.config.js`文件自定义webpack配置，这里修改了vue入口文件名字，然后在webpack里面也配置了，因为是electron所以必须要有一个入口文件，不想让它打包没办法我将它放在了public里面，然后在`package.json`里面配置了main字段和一些脚本，这样直接运行`npm run start`就能看到效果。

现在项目启动起来了，但是还有一个重要问题：热更新  ???



### 相关资料
[vue3修改webpack配置]（https://blog.csdn.net/u014440483/article/details/87267160）
[vue3中配置electron应用] (https://zhuanlan.zhihu.com/p/181015456?utm_source=wechat_session)

## vue和electron搭建开发桌面应用环境
在上面研究了vue3+electron,经过自己的一顿乱搞能启动起来，但是不能热更新也没找到相关介绍文档，而更多的是关于vue-cli + electron，这里记录一下，有直接的命令行就初始化一个项目不用自己配置，支持热更新。
```
npm install -g vue-cli
vue init simulatedgreg/electron-vue my-project
cd my-project
yarn # or npm install
yarn run dev # or npm run dev
```

### 相关资料
[electron-vue文档](https://simulatedgreg.gitbooks.io/electron-vue/content/cn/)