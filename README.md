# 欢迎大家来到保利威视帮助中心

---

* 代码高亮

```html
	<div class="container">
		<div class="navbar-header">
			<button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
				<span class="sr-only">Toggle navigation</span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
			</button>
			<a class="navbar-brand" href="http://www.polyv.net/">
				<img src="http://www.polyv.net/images/logo@2x.png" class="image-logo" alt="保利威视">
			</a>
		</div>

```

* 语法高亮

```ruby
	int buttonWidth = 100;
	int buttonsize = (int)self.bitRateButtons.count*30;
	int initHeight =(CGRectGetHeight(self.bitRateView.bounds)-buttonsize)/2;
	
	if (self.bitRateButtons!=nil) {
		for (int i=0; i<self.bitRateButtons.count; i++) {
			UIButton* _button = [self.bitRateButtons objectAtIndex:i];
			_button.bounds = CGRectMake(0, 0, pVideoControlBarHeight, 30);
			_button.frame = CGRectMake((CGRectGetWidth(self.bitRateView.bounds)-buttonWidth)/2, initHeight, buttonWidth, 30);
			initHeight+=30;
			
		}
	}

```