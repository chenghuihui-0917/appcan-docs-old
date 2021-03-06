# uexSegmentControl
   分段选择器插件

## 方法：
### [open](#open) 打开分段选择器
### [close](#close) 关闭分段选择器
### [setCurrentItem](#setCurrentItem) 设置当前选中项


## 监听方法：
### [onItemClick](#onitemclick) item被点击的监听方法
### [onDataChange](#ondatachange) 数据发生变化的监听方法

### open
  打开分段选择器
```
uexSegmentControl.open(json)
```
### 参数：
```
var json = {
    left:,//(可选) 左间距，默认0
    top:,//(可选) 上间距，默认0
    width:,//(可选) 宽度，默认屏幕宽度
    height:,//(可选) 高度，默认屏幕高度
    dataInfo:{//(必选) 数据
        allData:[],//(必选) 所有选择项的集合
        showData:[],//(必选) 导航条上显示的选择项的集合
        maxShow://(必选) 导航条上最多显示的选择项的个数
    }
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：

```
    var width = window.screen.width;
    var height = window.screen.height - 300;
    var param1 = {
        left:0,
        top:200,
        width:width,
        height:height,
        dataInfo:{
            allData:["头条", "娱乐", "体育", "北京", "财经", "科技", "段子", "图片", "汽车", "时尚",
				        "轻松一刻", "军事", "历史", "房产", "游戏", "彩票", "原创", "电台", "论坛", "博客",
				        "社会", "电影", "NBA", "中国足球", "国际足球", "CBA", "跑步", "手机",
                        "数码", "移动互联", "家居", "旅游", "健康", "读书", "酒香", "教育", "亲子", "葡萄酒",
                        "暴雪游戏", "情感", "政务"],
            showData:["头条", "娱乐", "体育", "北京", "NBA","科技", "段子", "旅游", "汽车", "时尚"],
            maxShow:25
        }
    };
    var data1 = JSON.stringify(param1);
    uexSegmentControl.open(data1);
```
运行效果：
默认打开状态：
![](http://i.imgur.com/ryLSVMU.png)

点击按钮进入选择编辑状态：
![](http://i.imgur.com/BrIlwtC.png)


### close
  关闭分段选择器
```
uexSegmentControl.close()
```
### 参数：
```
无
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：

```
    uexSegmentControl.close()
```

### setCurrentItem
  设置当前选中项
```
uexSegmentControl.setCurrentItem(json)
```
### 参数：
```
var json = {
    index://(必选) 索引
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：

```
    var param1 = {
        index:0
    };
    var data1 = JSON.stringify(param1);
    uexSegmentControl.setCurrentItem(data1);
```

### onItemClick
item被点击的监听方法
```
uexSegmentControl.onItemClick(json);
```
### 参数：
```
var json = {
    index:,//(必选) 被点击的元素的索引
    name://(必选) 被点击的元素的名称
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：
```
    uexSegmentControl.onItemClick = function(data){
        alert(data);
    }
```

### onDataChange
数据发生变化的监听方法
```
uexSegmentControl.onDataChange(json);
```
### 参数：
```
var json = {
    shows://(必选) 当前显示在导航条上的选择项集合
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：
```
    uexSegmentControl.onDataChange = function(data){
        alert(data);
    }
```