## 1.npm的使用
- npm：node package manager （package.json：描述了包的信息，包就是多个文件的集合）
- npm 中使用的时候，可以有2种方案：
  全局包：不能在代码中使用，只能在命令中使用
  本地包：只能在当前项目中使用

MacOS下全局node_modules目录地址：/usr/local/lib/node_modules/

### nrm npm nvm(淘宝源) cnpm
```
npm install nrm -g
nrm ls
nrm use taobao/cnpm/npm
nrm test => 可以测试下载速度
```
```
cuimengmengdeMacBook:node_modules cuimm$ nrm test

* npm ---- 1241ms
  yarn --- 1084ms
  cnpm --- 295ms
  taobao - 272ms
  nj ----- Fetch Error
  npmMirror  7122ms
  edunpm - Fetch Error

```


### 创建自己的全局包
- npm init => 生成 package.json 
- npm link => 链接，在全局的npm包下做一个快捷键

提示全局命令执行时对应的脚本，脚本必须增加`#! /usr/bin/env node`
```json
"bin": {
    "pack-cuimm": "./bin/test.js"
}
```

### 本地包
- 开发依赖：--save-dev(-D) 线上依赖：--save(-S)
- 默认情况下安装的模块是 --save




