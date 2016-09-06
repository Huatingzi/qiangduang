

#常用工具
  1. .gitignore
    - 这个是用来配置忽略文件
  >  /tmp.txt
     /js/*.js
     /js/*.*
     /*.*
  2. gh-pages
  3. git建立变量
    - `git push https.... `
    - `git remote add origin https.. `
  4. 版本回退
    - `git reset --hard Head~1`
      + Head指向最近的一次提交
    - `git reset --hard 版本号`
  5. 冲突
   - 在发现冲突时手动处理，处理之后还需要进行提交。
   - pull,会先下载文件，然后再自动合并远程代码与本地代码。


## git 拉取与推送代码到服务器
  - `git pull [地址]`
  - `git push [地址] [分支]`
  - `git push -u [地址] [分支]`
  - `git push [地址]`

## git使用ssh方式上传代码与github
  -ssh --keygen -t -rsa
  - 公钥和私钥 ,都是用户自成的.

### sourceTree , tortoiseGit


### npm
  - node package manager
  - 版本问题
  - 相互依赖的问题
  - bootsrap,juqery (库)
  - 项目管理只需要共享package.json文件
  [官网](https://www.npmjs.com)

#### npm安装
  - 安装完node就可以使用了

#### npm使用
  - 1.先进行初始化
    + 命令:`npm init ` //本质就是创建了一个package.json
  - 2.下载一些包
    + 命令:`npm install [包名] --save` 
      * 示例 `npm install jquery --save`
    默认会把文件下载到当前目录中的node_modules目录中
  - 3.删除一些包
    + 命令:`npm remove [包名] --save`
    默认会把对应的包删除，并在package.json文件中去除相关信息
  - 使用npm 全局安装的工具在C:\Users\[用户名]\AppData\Roaming\npm这个目录

### nrm 工具
  - 用来切换npm下载地址的
  - 安装命令:`npm install nrm  -g`
    + -g 表示全局安装，全局安装的目的是为了能够在命令行中使用,并且只需要安装一次  
	
	+ npm install -g nrm --registry  http://192.168.112.92/(这样可以访问指定的地址)
  
####nrm 使用
  - 1.列出所有的下载地址
    + 命令 `nrm ls`
  - 2.可以手动添加一些地址
    +  `nrm add [名字] [地址]`
    + 示例:`nrm add tmp http://www.baidu.com`
  - 3.切换下载地址
    + 命令:`nrm use [名字]`
    + 示例:`nrm use taobao`
  http://192.168.112.92/


### browser-sync
  - 可以用来自动刷新浏览器
  - 依赖于npm,需要使用npm安装
  - npm集成在node中
  安装:`npm install -g browser-sync`
  
  - 查看版本号:`browser-sync --version`

### browser-sync使用
  - 在项目根执行命令:`browser-sync start --server --files "./index.html"`
    + 执行命令后的窗口不要关
    + --files表示指定要监视的文件
    + 如果要监视多个文件，可以用逗号分隔 --files "./index.html,./style.css"

  - 还可以进行多浏览器兼容性调试

## Gulp
  - 自动化构建工具
  - grunt,webpack
  - 5个方法
  - 压缩，混淆，合并,
  - task(),js 压缩，合并,
  - src('')//匹配当前任务想要处理的文件
  - dest()//指定处理后的文件的存放路径.
  - watch // 监视文件的变化，文件一旦变化就调用指定的任务执行。
  - run(任务名)可以通过命令行调用任务

### Gulp安装
  - 命令:`npm install -g gulp-cli`

### gulp使用
  - 1.在当前项目安装gulp：`npm install gulp --save-dev`
  - 2.在当前项目根目录添加gulpfile.js文件，在写文件中写代码
  - 3.执行代码里的任务.：`gulp [任务名]`  示例:`gulp script`


### gulp插件
  - gulp-uglify:对js代码进行压缩，混淆
    + `npm install gulp-gulify --save-dev`
  - gulp-concat:对代码进行合并操作.
  - gulp-cssnano: 对css代码进行压缩


sublimeserver
powershell


packageControll官网
https://packagecontrol.io

window下工具
http://www.getwox.com/
https://github.com/Wox-launcher/Wox/releases
