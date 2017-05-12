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

## 浏览器兼容性
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

# 注意
这个项目基于 [qrcodejs](https://github.com/davidshimjs/qrcodejs)，但是现在作者已经停止了更新，为了让更多的人使用，建立这个项目，如果我已侵权，马上删除。
