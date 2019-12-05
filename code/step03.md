# Step 3. ボタンをクリックしたら消えるようにしよう

index.html

```html
<!DOCTYPE html>
<html>

<head>
	<title>Parcel Sandbox</title>
	<meta charset="UTF-8" />
</head>

<body>
	<div id="main">
		<button class="circle" id="1" onclick="remove()">1</button>
	</div>

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

document.remove = function() {
	document.getElementById("main").removeChild(document.getElementById("1"));
}
```

Next: [step04.md](./step04.md)
