
[toc]

## 使用express 搭建网站

1. 安装express模板生成器

    `npm install -g express-generator`

2. 安装 express

    加 -g 全局安装，不加在当前文件夹下安装

    `npm install -g express`

3. 使用express 生成工程
    `express app`

4.  创建好project之后还需要用npm进行添加依赖项和启动
    + 安装必备包
    `cd app&& npm install`
    + 启动服务
    `npm start`

5. 服务端口默认3000

    访问http://localhost:3000/

## jade ---> html

1. 安装之前应该先安装ejs

    `npm install ejs / cnpm install ejs -save`
2. 修改app.js

默认：

`app.set('view engine', 'html');`

改为
```
var ejs=require('ejs');
app.engine('html',ejs.__express);
app.set('view engine', 'html');
```
3. 把view目录下的jade 文件改为 html

+ 使用 npm install jade -g全局安装。

+ 然后在jade源文件那，使用 jade xxx.jade编译生成你需要的html
