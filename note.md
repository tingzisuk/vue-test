#vue

##目录结构描述
```
test：项目名称
  config：修改端口号等配置信息
  src：放写好的组件及其他资源
    App.vue：vue组件
    main.js：入口js文件
  index.html：html文件
```
##npm安装的包依赖管理相关
>1.--save-dev和--save的区别：使用npm install安装模块或插件的时候，--save-dev命令
会被写入package.json的devDependencies区块内，--save命令会被写入dependencies区块内；
devDependencies内的插件只用于开发环境，不用于生产环境（如：glup、webpack等只在开
发中用的包），而dependencies内的插件在上线时需要发布到生产环境（如：jquery等）。
