# Step 4. JavaScript から HTML 要素 を追加しよう

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

var elm = document.createElement("button");
elm.innerHTML = 1;
elm.setAttribute("id", 1); 
elm.setAttribute("class", "circle"); 
elm.setAttribute("onclick", "remove()");
document.getElementById("main").appendChild(elm);

document.remove = function() {
	document.getElementById("main").removeChild(document.getElementById("1"));
}
```

Next: [step05.md](./step05.md)
