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

### 3.效果图 ###

![Alt text](images/accordin_button.png "折叠面板和按钮")


## 三、操作表和数字角标 ##

### 1.操作表 ###

actionsheet一般从底部弹出，显示一系列可供用户选择的操作，actionSheet是从popover控件基础上演变而来，实际上就是一个固定在底部弹出的popover，因此dom结构和popover类似，只需要在含.mui-popover类的节点上添加mui-popover-bottom、mui-popover-action类

	<div class="mui-content">
		<div style="padding:20px;">
	    	<input type="button" class="mui-btn-blue" value="上传图片" onclick="showPop();" />
	    </div>    
	</div>
	<div id="sheet1" class="mui-popover mui-popover-bottom mui-popover-action ">
		<ul class="mui-table-view">
		  <li class="mui-table-view-cell">
		    <a href="#">拍照</a>
		  </li>
		  <li class="mui-table-view-cell">
		    <a href="#">從文件夾中選擇</a>
		  </li>
		</ul>
		<ul class="mui-table-view">
		  <li class="mui-table-view-cell">
		    <a href="#sheet1"><b>取消</b></a>
		  </li>
		</ul>
	</div>
	<script type="text/javascript">
		function showPop(){
			mui('#sheet1').popover('toggle');
		}
	</script>

### 2.数字角标 ###

数 字角标一般和其它控件（列表、9宫格、选项卡等）配合使用，用于进行数量提示。 角标的核心类是.mui-badge，默认为实心灰色背景；同时，mui还内置了蓝色（blue）、绿色(green)、黄色(yellow)、红色 (red)、紫色(purple)五种色系的数字角标

	<div style="margin-top: 20px;">
		<span class="mui-badge">1</span>
		<span class="mui-badge mui-badge-primary">2</span>
		<span class="mui-badge mui-badge-success">3</span>
		<span class="mui-badge mui-badge-warning">4</span>
		<span class="mui-badge mui-badge-danger">5</span>
		<span class="mui-badge mui-badge-royal">6</span>
	</div>

如果不需要底色，则添加类mui-badge-inverted

	<div style="margin-top: 20px;">
		<span class="mui-badge mui-badge-inverted">1</span>
		<span class="mui-badge mui-badge-primary mui-badge-inverted">2</span>
		<span class="mui-badge mui-badge-success mui-badge-inverted">3</span>
		<span class="mui-badge mui-badge-warning mui-badge-inverted">4</span>
		<span class="mui-badge mui-badge-danger mui-badge-inverted">5</span>
		<span class="mui-badge mui-badge-royal mui-badge-inverted">6</span>
	</div>

### 3.效果图 ###


![Alt text](images/actionSheet_badge.png "操作表和数字角标")


## 四、获取单选框和复选框的值 ##

### 1.获取复选框的值 ###

	<div class="mui-input-row mui-checkbox">
		<label for="">英语</label>
		<input type="checkbox" value="English" name="language" />
	</div>
	<div class="mui-input-row mui-checkbox">
		<label for="">法语</label>
		<input type="checkbox" value="Franch" name="language" />
	</div>
	<div class="mui-input-row mui-checkbox mui-left">
		<label for="">日语</label>
		<input type="checkbox" value="Japanese" name="language" />
	</div>
	<button id="button" onclick="getCheckBoxValue()">获取复选框的值</button>

 js代码如下

	function getCheckBoxValue(){
		var ck=document.getElementsByName('language')
		var checkVal=[];
		for(i=0;i<ck.length;i++){
			if(ck[i].checked){
				checkVal.push(ck[i].value);
			}
		}
		mui.toast(checkVal);
	}

### 2.获取单选框的值 ###

	<div class="mui-input-row mui-radio">
		<label for="">星期一</label>
		<input type="radio" name="weeks" value="Mon"/>
	</div>
	<div class="mui-input-row mui-radio">
		<label for="">星期二</label>
		<input type="radio" name="weeks" value="Tue"/>
	</div>
	<div class="mui-input-row mui-radio">
		<label for="">星期日</label>
		<input type="radio" name="weeks" value="Sun"/>
	</div>
	<button class="mui-btn mui-btn-success" onclick="getRadioValue()" >获取单选框的值</button>

js代码如下

	function getRadioValue(){
		var radio=document.getElementsByName('weeks');
		var checkVal=null;
		for(i=0;i<radio.length;i++){
			if(radio[i].checked){
				checkVal=radio[i].value;
			}
		}
		mui.toast(checkVal);
	}

3.列表式单选控件

	<div style="margin-top: 20px;">
		<ul class="mui-table-view mui-table-view-radio">
			<li class="mui-table-view-cell">
				<a class="mui-navigate-right">1</a>
			</li>
			<li class="mui-table-view-cell">
				<a class="mui-navigate-right">2</a>
			</li>
			<li class="mui-table-view-cell">
				<a class="mui-navigate-right">3</a>
			</li>
		</ul>
	</div>

js代码如下

	var list=document.querySelector('.mui-table-view-radio');
	list.addEventListener('selected',function(e){
		mui.toast("当前选中的为"+e.detail.el.innerText);
	});

### 4.效果图 ###

![Alt text](images/getCheckbox.png "复选框值获取")  

![Alt text](images/getRadio.png "单选框值获取")  


![Alt text](images/radioList.png "单选框值获取")  


## 五、时间选择器 ##

### 1.选择日期 ###

	<div class="mui-content">
		<div style="padding:15px;">
	        <button id='pickDateBtn' type="button" class="mui-btn">选择日期</button>
	    </div>
	    <div style="padding:15px;">
	        <button id='pickTimeBtn' type="button" class="mui-btn">选择时间</button>
	    </div>
	</div>

js代码


	document.getElementById('pickDateBtn').addEventListener('tap',function(){
		var dDate=new Date();
		//设置当前日期 不设置默认为今日日期
		dDate.setFullYear(2017,1,1);
		var minDate=new Date();
		minDate.setFullYear(2010,0,1);
		var maxDate=new Date();
		maxDate.setFullYear(2019,11,31);
		plus.nativeUI.pickDate(function(e){
			var d=e.date;
			mui.toast("您选择的日期是"+d.getFullYear()+"年"+(d.getMonth()+1)+"月"+d.getDate()+"日");
		},function(e){
			mui.toast('您没有选择日期');
		},{
			title:'请选择日期',
			date:dDate,
			minDate:minDate,
			maxDate:maxDate
		});
	});
	document.getElementById('pickTimeBtn').addEventListener('tap',function(){
		var dTime=new Date();
		dTime.setHours(6,1);
		plus.nativeUI.pickTime(function(e){
			var d =e.date;
			mui.toast("您选择的时间是："+d.getHours()+":"+d.getMinutes());
		},function(){
			mui.toast('您没有选择时间');
		},{
			title:'请选择时间',
			is24Hour:true,
			time:dTime
		});
	});

### 2.效果图 ###

![Alt text](images/datepicker.gif "时间选择器")  


## 六、对话框和表单 ##

### 1.mui.alert()普通提醒 ###

参数

	message     Type:string 提示框上显示的内容
	title       Type:string 提示框显示的标题
	btnValue    Type:string 提示框按钮的内容
    callback    Type:Function 提示框关闭后的回调函数
    type        Value:'div' 是否使用h5绘制的对话框

代码

	mui.alert('欢迎使用mui','Hello','yes',function(){
		mui.toast('您刚关闭了警告框');
	});


### 2.mui.confirm()消息提示框 ###

参数

	message     Type:string 提示框上显示的内容
	title       Type:string 提示框显示的标题
	btnValue    Type:string 提示框按钮的内容
    callback    Type:Function 提示框关闭后的回调函数
    type        Value:'div' 是否使用h5绘制的对话框

代码

	var btnArray = ['取消', '确定'];
	mui.confirm('真的要删除吗？','Hi...',new Arr('否','是'),funct({
	   if(e.index == 1){mui.toast('是');}else{mui.toast('否');}
	});

### 3.mui.prompt（）输入框 ###

参数

	message       Type: String 提示对话框上显示的内容
	placeholder   Type: String 编辑框显示的提示文字
	title         Type: String 提示对话框上显示的标题
	btnValue      Type: Array 提示对话框上按钮显示的内容
	callback      Type: Function提示对话框上关闭后的回调函数
	type         Value: 'div' 是否使用h5绘制的对话框

代码

	var btnArray=['取消','确定'];
	mui.prompt('请输入您的姓名','Hi...',new Array('取消','确定'),function(e){
		if(e.index==1){
			mui.toast(e.value);
		}else{
			mui.toast('您取消了输入');
		}
	});

### 4.表单元素 ###

所有包含在mui-input-row类中的input，textarea等元素都将被默认设置宽度属性为100%，将label元素和上述控件包裹在mui-input-group中可获得最好的排列

	<form class="mui-input-group">
		<div class="mui-input-row">
			<label for="">用户名</label>
			<input type="text" class="mui-input-clear" name="username" id="" value="" placeholder="请输入用户名"/>
		</div>
		<div class="mui-input-row">
			<label for="">密码</label>
			<input type="password" class="mui-input-password" placeholder="请输入密码" />
		</div>
		<div class="mui-input-row mui-search">
			<input type="search" class="mui-input-clear" placeholder="搜索" />
		</div>
		<div class="mui-button-row">
			<button type="button" class="mui-btn mui-btn-primary">提交</button>
			<button type="button" class="mui-btn mui-btn-danger">取消</button>
		</div>
	</form>


### 5.效果图 ###

![Alt text](images/dialog_input.gif "对话框")


## 七、轮播组件 ##

### 1.轮播组件 ###

轮播组件是mui提供的一个核心组件，在该核心组件的基础上，衍生除了图片轮播，可拖动式图文表格，可拖动式选项卡，左右滑动9宫格组件等。

示例代码

	<div class="mui-content">
		<div class="mui-slider">
			<div class="mui-slider-group mui-slider-loop">
				<!--循环轮播-->
				<div class="mui-slider-item mui-slider-item-duplicate">
					<a href=""><img src="../images/4.jpg"/></a>
				</div>
				<div class="mui-slider-item"><a href=""><img src="../images/1.jpg"/></a></div>
				<div class="mui-slider-item"><a href=""><img src="../images/2.jpg"/></a></div>
				<div class="mui-slider-item"><a href=""><img src="../images/3.jpg"/></a></div>
				<div class="mui-slider-item"><a href=""><img src="../images/4.jpg"/></a></div>
				<div class="mui-slider-item mui-slider-item-duplicate">
					<a href=""><img src="../images/1.jpg"/></a>
				</div>
			</div>
			<!--添加小圆点-->
			<div class="mui-slider-indicator">
				<div class="mui-indicator mui-active"></div>
				<div class="mui-indicator"></div>
			</div>
		</div>
	</div>

js代码

	<script type="text/javascript">
		mui.plusReady(function(){
			var gallery=mui('.mui-slider');
			gallery.slider({
				interval:3000  //自动播放周期 0为不自动播放
			});
		});
		document.querySelector('.mui-slider').addEventListener('slide',function(event){
			mui.toast('滑动到第'+(event.detail.slideNumber+1)+'张了');
		});
	</script>


### 2.效果图 ###

![Alt text](images/slide.gif "轮播组件")