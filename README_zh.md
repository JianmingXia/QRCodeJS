[English README](/README.md)

# QRCodeJS
由于自身的需求需要为二维码在中间添加图片

## 基础使用
```
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "https://github.com/JianmingXia/QRCodeJS");
</script>
```

其它使用：

```
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "https://github.com/JianmingXia/QRCodeJS",
	width: 128,
	height: 128,
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H,
	img_src: "img/user.jpg",
	img_width: 50
});
</script>
```

还可使用如下方法：

```
qrcode.clear(); // clear the code.
qrcode.makeCode("http://github.com"); // make another code.
```

## 属性
	- img_src：设置在二维码中间图片的url
		- 图片必须是可访问的，需要注意跨域的问题
	- img_width: 二维码中间图片的宽度
		- 如果没有设置，默认是二维码宽度的1/4
	- use_canvas: 是否使用canvas绘制（针对img_src属性被设置的情况下有效）
		- 前提是浏览器支持canvas，默认值是true；
		- 设置为false则使用img标签展示二维码，需要注意的是，这个时候速度会比较慢（需要等待img_src加载完成）

## 说明
	qrcode_dev.js是不稳定的调试版，当然，qrcode.js也不一定稳定，但是相对于qrcode_dev.js，会更加稳定。

## 浏览器兼容性
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

# 注意
这个项目基于 [qrcodejs](https://github.com/davidshimjs/qrcodejs)，但是现在作者已经停止了更新，为了让更多的人使用，建立这个项目，如果我已侵权，马上删除。
