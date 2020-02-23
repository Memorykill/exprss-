# express使用
精简版express文档
## express()
express()用来创建一个Express的程序。express()方法是express模块导出的顶层方法。

```javascript
var express = require('express');
var app = express();
```
## app.get()
设置什莫路径返回什莫路径（GET）
app.get(path [, callback ...])
|参数| 描述 | 默认值 |
|--|--|--|
| path | 页面的路径设置，值是字符串 | "/"(主目录) |
| callback | 这个路径是干什么的，值是函数字面量 |  None |

举个例子
```javascript
var express = require('express');
var app = express();
app.get('/', (req, res) =>{
  console.log("请求了localhost://3000/");
});
app.listen(3000);//可以打开浏览器搜索localhost://3000
```
这上面的函数里的req和res是express里的重要一部分，是express里简化的一大方面
 
|req| res |
|--|--|
|req.method|res.append(field [, value])|
|req.hosname|res.location(path)|
| req.baseUrl |res.send([body]) |
| req.ip | res.json([body]) |
| req.cookies | res.cookie(name, value [, options]) |
|req.query|res.sendFile(path [, options] [, fn])|
| req.path | res.end() |
|....|....|


![代码](https://img-blog.csdnimg.cn/2020022312554485.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1N5c3RlbV9zenM=,size_16,color_FFFFFF,t_70)
![输出](https://img-blog.csdnimg.cn/20200223125701937.png)


都拿来试试以及结果
相信你们也了解到了express文档大概都在说什莫无聊的api了，**[传送门](http://www.expressjs.com.cn/4x/api.html)**：http://www.expressjs.com.cn/4x/api.html
 
 
 
 

 

## app.listen()
服务器的必须组件，调用此函数才能在浏览器中打开对应的页面
app.listen([port[, host[, backlog]]][, callback])

```javascript
var express = require('express');
var app = express();
app.get('/', function (req, res) {
  res.send('hi');
});
app.listen(3000);//可以打开浏览器搜索localhost://3000
```

相信你们也了解到了express文档大概都在说什莫无聊的api了，**[传送门](http://www.expressjs.com.cn/4x/api.html)**：http://www.expressjs.com.cn/4x/api.html
