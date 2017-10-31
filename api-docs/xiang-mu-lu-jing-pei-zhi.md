######  注：测试环境api接口域名和链接地址域名一般相同，但线上环境链接地址域名和接口地址不同，请注意不要混淆HybridParams.url和HybridParams.pc用法。

建议：在项目上线之前，将分享及相关的地址链接切换为绝对路径，防止出错。

#### 

#### 一、活动专用域名形式

**注意：活动js统一存放入static/h5/js/js/....**

hybridParams.js域名封装函数

var HybridParams = require\('../modules/hybridParams.js'\);

| HybridParams.url | api接口域名 | https://pc121.yonglibao.com |
| :--- | :--- | :--- |
| HybridParams.pc | pc文件夹地址域名 | https://pc121.yonglibao.com/ |
| HybridParams.h5 | h5文件夹地址域名 | https://pc121.yonglibao.com/h5/ |
| HybridParams.static | static文件夹地址域名 | https://pc121.yonglibao.com/static/ |
| HybridParams.token | 用户token |  |



#### 二、永利宝线上项目

不同的位置的域名配置函数存放在不同的js文件中，项目调用时，请参考相同文件夹下的其他项目的配置调用方法。

#### **一般**

h5:  存放在src/static/h5/js/modules/hybridParams.js  调用var params = require\("../modules/hybridParams.js"\);

pc:存放在src/static/pc/js/modules/params.js调用var params = require\('../../modules/params.js'\)

每个配置的各个参数见上表所示

