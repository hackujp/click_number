# 色をランダムにする

index.html

```html
<!DOCTYPE html>
<html>

<head>
	<title>Parcel Sandbox</title>
	<meta charset="UTF-8" />
</head>

<body>
	<div id="main"></div>

	<script src="src/index.js">
	</script>
</body>

</html>
```

src/style.css

```css
body {
	font-family: sans-serif;
}

.circle {
	background-color: skyblue;
	border-radius: 30px;
	height: 60px;
	width: 60px;
	font-size: 24px;
	position: absolute;
}
```

src/index.js

```js
import "./styles.css";

for (var num=9;num>0;num--) {
	var elm = document.createElement("button");
	elm.innerHTML = num;
	elm.setAttribute("id", num); 
	elm.setAttribute("class", "circle"); 
	var function_name = "remove(" + num + ")" 
	elm.setAttribute("onclick", function_name);
	document.getElementById("main").appendChild(elm);

	var left = 10;
	var top = 100;

	left = left + Math.floor(Math.random() * 400);
	top = top + Math.floor(Math.random() * 600);

	document.getElementById(num).style.left = "" + left + "px" ;
	document.getElementById(num).style.top = "" + top + "px" ;
	
	var red = 100 + Math.floor(Math.random() * 155);
	var green = 100 + Math.floor(Math.random() * 155);
	var blue = 100 + Math.floor(Math.random() * 155);

  	document.getElementById(num).style.backgroundColor = "rgb(" + red + "," + blue + "," + green + ")";
}

var next = 1;
document.remove = function (id) {
	if (id === next) {
		document.getElementById("main").removeChild(document.getElementById(id));
		next = next + 1;
	}
}
```

応用編
* [丸の大きさをランダムにする](./advance01.md)
* [経過時間で数字を再配置する](./advance03.md)
