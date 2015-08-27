# 前端集成自动化项目构建方案Hawk


<img src="https://raw.githubusercontent.com/qihong1983/generator-hawk/master/app/logo.png"  />


by 小洪 qihongbin@163.com

## Generator-Hawk 方案简介

> Generator-Hawk 是web前端项目脚手架方案，用来生成项目代码骨架，你可以方便的基于此结构来开发你的项目，并享用到 web前端的诸多优秀特性。

### Generator-Hawk 安装

> npm install -g yo generator-hawk

### Generator-Hawk 所需要的环境

> node
> gitbash
> charles


## 环境配置

### gitbash 中文环境配置

> gitbashgitbashgitbashgitbashgitbashgitbash

## Generator-Hawk 方案的使用 

> 方案的使用方案的使用方案的使用  

## Generator-Hawk 组成

<img src="https://raw.githubusercontent.com/qihong1983/generator-hawk/master/app/tools.jpg" style="width:487px; height:auto;" />


### 主要工具

> Yeoman：脚首架

> Gulp:打包/构建/预发/发布/开发环境

> Bower:组件管理依赖关系

> Gitlab：代码仓库


### 工具下载

> http://msysgit.github.io/   gitbash下载

> http://nodejs.org         nodejs下载

> $npm install –g yo 			  #yeaman安装

> $npm install –g gulp 	 	  #gulp安装

> $npm install –g bower 		  #bower安装

> $npm install –g generator-hawk  #generator-hawk安装

## 走起

<img src="https://raw.githubusercontent.com/qihong1983/generator-hawk/master/app/zouqi.jpg"  />


### 基本命令-- yo & gulp

#### yo初始化

>yo hawk:h:打印帮助

>yo hawk:初始化一个标准的Project

>yo hawk:初始化一个页面

>yo hawk:mod:初始化一个模块

>yo hawk:widget:初始化一个组件

#### gulp打包

> gulp dev: 本地运行 

> gulp dev64: 本地运行图片base64编码

> gulp qa: 打包到测试环境 并自动提交到ftp服务器

> gulp qa64: 打包到测试环境图片base64编码 并自动提交到ftp服务器

> gulp online:  打包成线上环境 并自动提交到ftp服务器

> gulp online64: 打包成线上环境64 并自动提交到ftp服务器

> gulp onlineDebug: 打包成线上环境 不提交到ftp服务器

> gulp online64Debug: 打包成线上环境 不提交到ftp服务器 

### 目录结果 & 代码

#### 目录结果


```
./
├── gulpfile.js              项目构建主任务
├── package.json              项目配置文件
├── README.md                 项目自述文件
├── build/                    构建目录
├── doc/                      文档存放目录
├── .bower.json               组件安装源配置(gitlab or github)
├── .bowerrc                  
├── .editorconfig
├── .gitignore
├── abc.json 				  项目配置文件
└── src/                      源码目录
    ├── config.js             项目config.js
    ├── mods/  
    │   │            
    │   ├── mod1			   业务公用模块目录
    │	│	├── demo.html
    │	│	├── mod1.html
    │	│   ├── mod1.js
    │	│	└── mod1.css
    │	└── mod2
    │		├── demo.html
    │		├── mod2.html
    │		├── mod2.js
    │		└── mod2.css
    │		
    ├── widgets/              组件目录（通用组件）
    │   │
    │   ├── widget1/
	│	│	├── demo.html
	│	│	├── widget1.js
    │   │   └── widget1.css
    │   └── widget2/          
    │		├── demo.html
    │		├── widget2.js
    │       └── widget2.css
    └── pages/                         
        └── page1/             
            ├── page1.js      
            ├── page1.sss        
            └── page1.html       
            ...
```



## 插件的使用(gulpfile.js)
```javascript
var gulp = require('gulp'),
  hawkcss = require('gulp-hawkcss');

gulp.task('default', function() {
  gulp.src('./*.html')
    .pipe(hawkcss())
    .pipe(gulp.dest('dest/'));
});
```

## 示例html代码

> http://a.cdn.cn/??assets/a1.css,assets/a2.css,assets/a3.css

```html
<!DOCTYPE html>
<html>
<head lang="zh-cmn-Hans">
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="renderer" content="webkit">
    <link rel="stylesheet" href="assets/mian.css" />
    <!-- css:start -->

    <!-- css:end -->

    <title>cssCombo</title>
</head>
<body>
    <link rel="stylesheet" href="assets/a1.css" />
    <link rel="stylesheet" href="assets/a2.css" />
    <div class="a1">
        a1
    </div>
    <div class="a2">
        a2
    </div>

    <link rel="stylesheet" href="assets/a3.css" />
    <div class="a3">
        a3
    </div>


</body>
</html>
```


