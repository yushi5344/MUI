# MUI学习 demo代码

## 一、 项目创建、基础布局  
 
### 1、头部 ##
核心css  mui-bar mui-bar-nav

    <header class="mui-bar mui-bar-nav">
        <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
        <h1 class="mui-title">hello</h1>
    </header>

### 2、主体部分 ##
核心css mui-content

	<div class="mui-content">
	    主体部分....
	</div>

### 3、完整代码演示 ##

	<body>
	<div>
	<header class="mui-bar mui-bar-nav">
	    <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
	    <h1 class="mui-title">hello</h1>
	</header>
	<div class="mui-content">
	    内容部分....
	</div>
	</body>

## 二、accordion（折叠面板）、button（按钮） ##

### 1.折叠面板 ###
折叠面板从二级列表中演化而来，dom结构和二级列表类似，如下：

	<div class="mui-content">
		<div class="mui-card">
			<ul class="mui-table-view">
				<li class="mui-table-view-cell mui-collapse">
					<a class="mui-navigate-right">季节</a>
					<div class="mui-collapse-content">
						<p>春</p>
					</div>
					<div class="mui-collapse-content">
						<p>夏</p>
					</div>
					<div class="mui-collapse-content">
						<p>秋</p>
					</div>
					<div class="mui-collapse-content">
						<p>冬</p>
					</div>
				</li>
				<li class="mui-table-view-cell mui-collapse mui-active">
					<a class="mui-navigate-right">节日</a>
					<div class="mui-collapse-content">
						<p>春分</p>
					</div>
					<div class="mui-collapse-content">
						<p>清明</p>
					</div>
					<div class="mui-collapse-content">
						<p>秋分</p>
					</div>
					<div class="mui-collapse-content">
						<p>冬至</p>
					</div>
				</li>
			</ul>
		</div>
	</div>
可以在折叠面板中放置任何内容；折叠面板默认收缩，若希望某个面板默认展开，只需要在包含.mui-collapse类的li节点上，增加.mui-active类即可；mui官网中的方法说明，使用的就是折叠面板控件  
 
**注意**：  
1、折叠面板布局必须在 mui-content下   
2、外层使用 mui-card 包裹产生边缘    

### 2.按钮 ###

	<div>
		<button type="button" class="mui-btn">默认</button>
		<button type="button" class="mui-btn mui-btn-primary">蓝色</button>
		<button type="button" class="mui-btn mui-btn-success">绿色</button>
		<button type="button" class="mui-btn mui-btn-warning">黄色</button>
		<button type="button" class="mui-btn mui-btn-danger">红色</button>
		<button type="button" class="mui-btn mui-btn-royal">紫色</button>
	</div>

无底色的按钮，继承自父类

	<div style="margin-top: 20px;">
		<button type="button" class="mui-btn mui-btn-outlined">默认</button>
		<button type="button" class="mui-btn mui-btn-primary mui-btn-outlined">蓝色</button>
		<button type="button" class="mui-btn mui-btn-success mui-btn-outlined">绿色</button>
		<button type="button" class="mui-btn mui-btn-warning mui-btn-outlined">黄色</button>
		<button type="button" class="mui-btn mui-btn-danger mui-btn-outlined">红色</button>
		<button type="button" class="mui-btn mui-btn-royal mui-btn-outlined">紫色</button>
	</div>