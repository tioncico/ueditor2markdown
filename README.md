# ueditor2markdown
ueditor2markdown   nodejs

```js
// 引入 markdown-it 库
TurndownService = require('./ueditor2markdown.js');
// 创建 markdown-it 实例
// 引入 fs 模块
var fs = require('fs');

// 读取文件，并在读取完成后调用回调函数
fs.readFile('../test.html', 'utf8', function(err, data) {
    // 如果读取过程中出错，抛出错误
    if (err) throw err;
    html = data;
    var turndownService2 = new TurndownService();
    var text = turndownService2.turndown(html, {gfm: true});
// 输出 HTML 代码
    console.log(text);
});


```

```shell
node app.js
```
