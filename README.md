# Elevene-M_Js
Use  JSP/HTML   order by  juqery.js


/*#################################################################################*/
	//微信JS SDK认证，接口
	//微信JS
	alert(location.href.split('#')[0])
	wx.config({
	    debug: true, // 开启调试模式,调用的所有api的返回值会在客户端alert出来，若要查看传入的参数，可以在pc端打开，参数信息会通过log打出，仅在pc端时才会打印。
	    appId: ''+appid+'', // 必填，公众号的唯一标识
	    timestamp: ''+timestamp+'', // 必填，生成签名的时间戳
	    nonceStr: ''+nonceStr+'', // 必填，生成签名的随机串
	    signature: ''+signature+'',// 必填，签名，见附录1
	    jsApiList: ['onMenuShareAppMessage'] // 必填，需要使用的JS接口列表，所有JS接口列表见附录2
	});

	wx.ready(function(){
		 alert("【分享接口注册成功】");
		var reaction=path+"/index!toaddonmv2.action?tid="+tid+"&jingquid="+jingquid+"&weixinFUser="+mappid;
		 
		document.querySelector('#onMenuShareAppMessage').onclick = function () {
	 		wx.onMenuShareAppMessage({
	 		    title: '分享嗨起来，获利！！！', // 分享标题
	 		    desc: '聚众好友，返利多多', // 分享描述
	 		    link: ''+reaction+'', // 分享链接
	 		    imgUrl: '../images/qb.png', // 分享图标
	 		    type: '', // 分享类型,music、video或link，不填默认为link
	 		    dataUrl: '', // 如果type是music或video，则要提供数据链接，默认为空
	 		    success: function () { 
	 		        // 用户确认分享后执行的回调函数
	 		    },
	 		    cancel: function () { 
	 		        // 用户取消分享后执行的回调函数
	 		    }
	 		});
	 	});
	});
