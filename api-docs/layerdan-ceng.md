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

类型：String，默认：''

skin不仅允许你传入layer内置的样式class名，还可以传入您自定义的class名。这是一个很好的切入点，意味着你可以借助skin轻松完成不同的风格定制。目前layer内置的skin有：_layui-layer-lanlayui-layer-molv_，未来我们还会选择性地内置更多，但更推荐您自己来定义。

### 5.area-宽高

类型：String/Array，默认：'auto'

在默认状态下，layer是宽高都自适应的，但当你只想定义宽度时，你可以_area: '500px'_，高度仍然是自适应的。当你宽高都要定义时，你可以_area: \['500px', '300px'\]_

### 6.offset-坐标

类型：String/Array，默认：垂直水平居中

offset默认情况下不用设置。但如果你不想垂直水平居中，你还可以进行以下赋值，具体见[http://www.layui.com/doc/modules/layer.html\#type官网API](http://www.layui.com/doc/modules/layer.html#type官网API)

### 7.btn - 按钮

类型：String/Array，默认：'确认'

信息框模式时，btn默认是一个确认按钮，其它层类型则默认不显示，加载层和tips层则无效。当您只想自定义一个按钮时，你可以_btn: '我知道了'_，当你要定义两个按钮时，你可以_btn: \['yes', 'no'\]_。当然，你也可以定义更多按钮，比如：_btn: \['按钮1', '按钮2', '按钮3', …\]_，按钮1的回调是yes，而从按钮2开始，则回调为btn2: function\(\){}，以此类推。如：

```js
layer.open({  

  content: 'test'

  ,btn: ['按钮一', '按钮二', '按钮三']

  ,yes: function(index, layero){

    //按钮【按钮一】的回调

  }

  ,btn2: function(index, layero){

    //按钮【按钮二】的回调

    //return false 开启该代码可禁止点击该按钮关闭

  }

  ,btn3: function(index, layero){

    //按钮【按钮三】的回调

    //return false 开启该代码可禁止点击该按钮关闭

  }

  ,cancel: function(){ 

    //右上角关闭回调

    //return false 开启该代码可禁止点击该按钮关闭

  }

});
```

### 8.btnAlign-按钮排列

类型：String，默认：r

你可以快捷定义按钮的排列位置，btnAlign的默认值为r，即右对齐。该参数可支持的赋值如下：

| 值 | 备注 |
| :--- | :--- |
| btnAlign:'l' | 按钮左对齐 |
| btnAlign:'c' | 按钮居中对齐 |
| btnAlign:'r' | 按钮右对齐。默认方式 |

### 9.closeBtn-关闭按钮

类型：String/Boolean，默认：1

layer提供了两种风格的关闭按钮，可通过配置_1_和_2_来展示，如果不显示，则_closeBtn: 0_

### 10.更多属性详见layer.js的API[http://www.layui.com/doc/modules/layer.html\#type官网API](#)

## EXAMPLE



```
 layer.open({
  
    type: 1,

    skin: 'layui-layer-rim', //加上边框

    area: \['420px', '240px'\], //宽高

    content: 'html内容'
  
 }); 
```



