---
layout: slides
title: MTEC1002 - Canvas
---

<section markdown="block" class="title-slide">

# Canvas Preview

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Git - Setting Up Repositories

{% highlight html %}
<html>
<head>
	<title></title>
</head>
<body>
<canvas id="sketch" width="300" height="225">
</canvas>
<script>
// http://diveintohtml5.info/canvas.html
// https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Canvas_tutorial/Drawing_shapes#Arcs
var sketch = document.getElementById('sketch');
var context = sketch.getContext("2d");
//context.fillRect(50, 25, 150, 100);
for (var i = 1; i <= 10; i++) {
	if(i % 2 == 0) {
		context.fillRect(i * 30, 1, 20, 20);

	} else {
		context.beginPath();

		context.arc(i * 30 + 10, 10, 10, 0, 2* Math.PI, true);
		ctx.closePath();
		context.fill();

	}
}
</script>
</body>
</html>
{% endhighlight %}
</section>
