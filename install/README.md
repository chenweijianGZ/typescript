## TypeScript 安装及开发环境配置
### 一、安装Node.js
TypeScript源码需要进行编译以后才能运行，Node.js提供了编译环境.</br>
安装文件下载地址：[Node.js官网](http://nodejs.cn/)

### 二、安装TypeScript编译工具
安装好Node.js后，打开cmd窗口,输入一下命令:  `npm install -g typescript`,全局安装typescript包，安装成功后即可编译Typescript文件.

* 查看版本 `tsc -v`
* 编译文件 `tsc fileName.js`
* 安装库的d.ts文件 `npm install --save-g @types/node`

### 三、使用Visual Studio Code进行开发

####1.创建tsconfig.json</br>
  typescript 的项目都需要一个tsconfig.json  
  输入命令`tsc --init` 会自动创建tsconfig.json.  
  建议修改配置如下图:

	{
	  "compilerOptions": {
		  /*编译为es5 兼容浏览器 可选es5 || es6*/
	      "target": "es5",
	      "noImplicitAny": false,
		  /*使用commonjs规范 可选commonjs || AMD || es2016*/
	      "module": "commonjs",
		  /*编译后是否清除注释*/
	      "removeComments": true,
		  /*是否索引源码*/
	      "sourceMap": true,
		  /*输出目录*/
	      "outDir": "js",
		  /*是否兼容JS文件*/
	      "allowJs": true
	  },
	  "include":[
	      "ts"
	  ],
	  "exclude": [
		  /*不监听文件*/
	      "js",
	      "node_modules"
	  ]
	}
####2.配置编译TypeScript
  打开vscode，按`ctrl+shift+b`,就会出现一次编译和监听编译两个选择，分别如下：

* `tsc:build - xx/tsconfig.json` 一次编译
* `tsc.watch - xx/tsconfig.json` 监听编译

到此一个ts项目就配置完成.

    

