# JS-mCarousel 
卡片式旋转木马


#### HTML结构
```html
<div class="wrapper" id="wrapper">
	<ul class="scroller">
		<li>1</li>
		<li>2</li>
		<li>3</li>
		<li>4</li>
		<li>5</li>
	</ul>
</div>
```

#### 加载JS
```html
<script type="text/javascript" src="mCarousel.js"></script>
```

#### 实例化 
```js
var carousel = new mCarousel('#wrapper', {
	// index: 2, 
	scale: 0.6,
	// active: 'active',
	// duration: 500,
	// locked: true,
	before: function() {
		console.log('切换开始')
	},
	after: function() {
		console.log('切换结束')
	}
});
document.querySelector('.next').onclick = function(){
	carousel.next();
};
document.querySelector('.prev').onclick = function(){
	carousel.prev();
};
```