# MicroDevelopment SampleDemo sample-html

> **在开始往下看之前，请务必确认看过微开发相关的全部文档**

[微开发官方文档](https://docs.microdevelopment.dev)

本仓库假设就为你的业务代码，静态HTML。

你需要的 CSS  和  JS 都被分解成了独立的仓库。

- [https://github.com/micro-development/sample-js](https://github.com/micro-development/sample-js)
- [https://github.com/micro-development/sample-css](https://github.com/micro-development/sample-css)


## Cli Install

[微开发官方脚手架文档](https://docs.microdevelopment.dev/cli)

### 安装脚手架

```bash
npm install -g micro-development-cli
```

### 安装微开发依赖（git仓库）

```bash
md-cli install # or md-cli i
```

上面命令执行完会输出以下内容：
```bash
全部开始安装...

安装仓库：https://github.com/micro-development/sample-js.git 开始...
Cloning into 'git-static/sample-js!!!master'...
remote: Enumerating objects: 8, done.
remote: Counting objects: 100% (8/8), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 8 (delta 1), reused 4 (delta 1), pack-reused 0
安装仓库：https://github.com/micro-development/sample-js.git 成功

安装仓库：https://github.com/micro-development/sample-css.git 开始...
Cloning into 'git-static/sample-css!!!master'...
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 11 (delta 2), reused 6 (delta 1), pack-reused 0
安装仓库：https://github.com/micro-development/sample-css.git 成功

安装仓库：https://github.com/micro-development/sample-css.git 开始...
Cloning into 'git-static/sample-css!!!bg_custom'...
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 11 (delta 2), reused 6 (delta 1), pack-reused 0
安装仓库：https://github.com/micro-development/sample-css.git 成功

全部安装结束（Total 3）：（Success 3 ，Error 0 ）
```
同时，在根目录增加一个文件夹：`git-static` ，下面有三个目录：

- git-static/sample-js!!!master
- git-static/sample-css!!!master
- git-static/sample-css!!!bg_custom
  
具体原理，就不再细说了，参考官方文档说明。

### 启动

把 `index.html` 拖到浏览器，能看到两个效果：

1. 页面背景为红色,来自 `https://github.com/micro-development/sample-css` 仓库的 `master` 分支的 `sample.css`
2. 打开控制台，打印出日志：`sample-js sample.js`，来自 `https://github.com/micro-development/sample-js` 仓库的 `master` 分支的 `sample.js`


**现在，你把 `index.html` 中第 7 行注释打开，再刷新页面，会发现页面变为了蓝色。** 来自 `https://github.com/micro-development/sample-css` 仓库的 `bg_custom` 分支的 `sample.css` ，把不同的分支安装进来，切换引用或覆盖，即可。

