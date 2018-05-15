## 1、移动端fixed和input获取焦点软键盘弹出影响定位的问题?
在某些安卓机下，键盘弹起会引起窗口高度（html标签的高度）变小，而fixed定位是相对于html根元素的，所以会被顶上来了。所以你可以在页面加载完之后，用js获取窗口的高度赋值给html或者按钮的父元素，然后把按钮的定位改成absolute应该就可以了吧。即：
```javascript
	var h=$(window).height();
	    $(window).resize(function() {
	        if($(window).height()<h){
	            $('.footer').hide();
	        }
	        if($(window).height()>=h){
	            $('.footer').show();
	        }
	    });

	});
```

## 2.移动端页面默认代码添加

### 防止缩放，适配手机 
```javascript
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
```

### 防止ios识别手机号 
```javascript
<meta content="telphone=no,email=no" name="format-detection" />
```