#搭建vue开发环境：
>vue依赖于node.js的npm管理工具实现，而npm在国内运行太慢安装淘宝cnpm

##下载[node.js](http://nodejs.cn)
>node -v 查看node版本

##安装淘宝npm镜像cnpm
>命令行输入npm install -g cnpm --registry=http://registry.npm.taobao.org安装  
cnpm -v 查看cnpm版本

##node.js环境配置
>这里的环境配置主要配置的是npm安装的全局模块所在的路径，以及缓存cache的路径，之所以要
配置，是因为以后在执行类似：npm install express [-g]（后面的可选参数-g，g代表global全
局安装的意思）的安装语句时，会将安装的模块安装到C:\Users\用户名\AppData\Roaming\npm路
径中，占C盘空间。 
 
1.将全模块所在路径和缓存路径放在node.js安装的文件夹中，则在安装的文件夹F:\nodejs下创建
两个文件夹node_global及node_cache  
2.打开cmd命令窗口，输入  
npm config set prefix "F:\nodejs\node_global"  
npm config set cache "F:\nodejs\node_cache" 
> 注:prefix与路径间有空格，没有空格会配置失败 

3.设置环境变量  
我的电脑--属性--高级系统设置--高级--环境变量  
系统变量--新建NODE_PATH--输入F:\nodejs\node_global\node_modules  
用户变量--修改PATH的npm部分--F:\nodejs\node_global

##安装vue-cli脚手架
>命令行输入cnpm install -g vue-cli（全局安装 vue-cli）  
vue -V 查看vue版本（V为大写）

##创建vue项目
>1.进入到目录下，命令行输入vue init webpack test（test为文件名，基于webpack的项目）  
2.一直回车，出现 vue-route，项目中需要用到 输入Y回车，出现是否需要js语法检测，不需要用
到 输入N回车，进入项目文件，命令行输入cd test回车  
3.项目各个模块之间相互依赖，命令行输入cnpm install安装依赖  
4.测试下载的模板正常运行，命令行输入cnpm run dev启动项目，根据命令行的端口号在浏览器
中测试  
(根目录下config的index.js可修改端口号等配置信息)

#安装Git
>1.初始化项目使之成为git仓库  
进入项目目录，git init初始化仓库，创建后出现.git隐藏文件夹（用来管理git仓库所需要的东西）  
2.github上New repository--create repository创建或者使用已有的仓库  
需要配置用户信息以及SHH key  
git remote add origin https://github.com/tingzisuk/vue-test.git关联远程库  
(https://github.com/tingzisuk/vue-test.git是github上创建的或已有的仓库的http地址，在
git客户端直接按 insert 即可粘贴内容)  
查看关联库的信息：
git remote -v 列出已关联的库，带有URL  
git remote 列出已关联的库，不带url  
git remote show 库名称  查看某一个指定的库  
git add 将文件提交到库，即提交到暂存区  
git add .（.表是工作区所有的变化，也就是你对项目做了修改的文件，但不包括删除的文件）  
git status 查看当前库的状态  
git commit -m "注释内容" 输入对这次提交的说明  
------------------------------interrupt----------------------------  
git push -u xyd master提交到远程库  
git push -u origin master上传本地项目

 



