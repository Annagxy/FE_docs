# layer.js弹层文档

我们项目中用到弹窗/层，统一使用layer.js

layer.js已经封装至项目中，调用路径

**&lt;script src="&lt;%= static.lib %&gt;/layer/layer.m.js"&gt;&lt;/script&gt;**

### 1.type-基本层类型

类型：Number，默认：0

layer提供了5种层类型。可传入的值有：_0_（信息框，默认）_1_（页面层）_2_（iframe层）_3_（加载层）_4_（tips层）。 若你采用_layer.open\({type: 1}\)_方式调用，则type为必填项（信息框除外）

### 2.title-标题

title支持三种类型的值，若你传入的是普通的字符串，如**title :'我是标题'**，那么只会改变标题文本；

若你还需要自定义标题区域样式，那么你可以**title: \['文本', 'font-size:18px;'\]**，数组第二项可以写任意css样式；

如果你不想显示标题栏，你可以**title: false**

### 3.content-内容

类型：String/DOM/Array，默认：''

content可传入的值是灵活多变的，不仅可以传入普通的html内容，还可以指定DOM，更可以随着type的不同而不同。

### 4.skin-样式类名







