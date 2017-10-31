我们项目中用到的微信分享方法的调用；

```
var weixin = require("../modules/weixin.jdk.js");//调用微信jdk




weixin.config({

    title: "标题",

    desc: "内容",

    imgUrl: 图片地址,

    link: 链接地址'

},false);
```

#### 微信分享的图片要求：尺寸为300\*300，大小应该控制在32k以内，最好为30k以内。



