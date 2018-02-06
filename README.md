1.移动端fixed和input获取焦点软键盘弹出影响定位的问题?
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


2.移动端页面默认代码添加
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
防止缩放，适配手机
<meta content="telphone=no,email=no" name="format-detection" />
防止ios识别手机号