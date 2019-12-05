# Step 8. ボタンを数の小さい順に押すと消えていくようにしよう

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

for (var num=1;num<10;num++) {
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
}

var next = 1;
document.remove = function (id) {
	if (id === next) {
		document.getElementById("main").removeChild(document.getElementById(id));
		next = next + 1;
	}
}
```

Next: [step09.md](./step09.md)
