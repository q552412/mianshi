

第一章 面试的流程

​		1.1 面试的形式

​				1.1.1 电话面试

​				1.1.2 共享桌面远程面试

​				1.1.3 现场面试

​		1.2 面试的环节

​				1.2.1 HR面试环节

​				1.2.2 技术面试环节  

​				1.2.3 应聘者提问环节

​		1.3 本章小结

第二章 面试题基础篇

​		2.1 HTML面试题				

​				面试题：行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

​				面试题：页面导入样式时，使用link和@import有什么区别？

​				面试题：title与h1的区别、b与strong的区别、i与em的区别？

​				面试题：img标签的title和alt有什么区别？

​				面试题：png、jpg、gif 这些图片格式解释一下，分别什么时候用？

​		2.2 CSS面试题

​				面试题：介绍一下CSS的盒子模型

​				面试题：CSS选择符有哪些？哪些属性可以继承？

​				面试题：CSS优先级算法如何计算？

​				面试题：用CSS画一个三角形

​				面试题：一个盒子不给宽度和高度如何水平垂直居中？

```
1. flex
2. 定位 + transfrom
```

​				面试题：display有哪些值？说明他们的作用。

​				面试题：对BFC规范(块级格式化上下文：block formatting context)的理解？

```
触发了BFC的规范或者特性，就会让其中的子元素做任何改变都不会影响上面的元素和下面的元素

overflow: hidden;overflow: scroll;
float:不是none
....
```

​				面试题：清除浮动有哪些方式？

```
1. 触发BFC
2. after
		ul:after{
			content: '';
			display: block;
			clear: both;
	}
```

​				面试题：在网页中的应该使用奇数还是偶数的字体？为什么呢？

​				面试题：写一个左中右布局占满屏幕，其中左、右俩块固定宽200，中间自适应宽，要求先加载中间块，请写出结构及样式。

​				面试题：什么是CSS reset？

​				面试题：css sprite是什么,有什么优缺点

​				面试题：display: none;与visibility: hidden;的区别

​				面试题：position有哪些值?有什么作用? 【特别多公司问】

​				面试题：line-height和height有什么区别？

​				面试题：opacity 和 rgba区别

​		2.3  JavaScript基础面试题

​				面试题：延迟加载JS有哪些方式？

```
async、defer

<script type="text/javascript" src='a.js' defer></script>
<script type="text/javascript" src='a.js' async></script>

defer 按照顺序执行 
async 是谁先加载完了，谁执行

场景：
	1.如果文件存在依赖关系就用defer
  2.有一些特殊的js文件其中代码是特别重要的可以async提前加载
```

​				面试题：JS数据类型有哪些？

```
基本：String、Boolean、Number、undefined、null、Symbol【es6】、Bigint【谷歌6、7】
引用：Object
```

​				面试题：null和undefined的区别

```
JavaScript的最初版本是这样区分的：null是一个表示"无"的对象（空对象指针），转为数值时为0；undefined是一个表示"无"的原始值，转为数值时为NaN。
```

​				面试题：JS数据类型考题

​				面试题：==和===有什么不同

​				面试题：JS微任务和宏任务

```
1. js是单线程语言（这个和js特性有关系：因为js是交互是做交互的）
2. js执行流程 ： 同步==》异步
3. 微任务：promise.then 、 promise.catch ...
	 宏任务：script标签、定时器、事件
4. 执行：因为script标签是宏任务所以执行是。
	碰到script【第一个宏任务】进入script代码中，执行同步==》微任务==》下一个宏任务==》同步==》微任务清空==》下一个宏
```

​				面试题：JS作用域考题

```
1. 作用域：先在本层找，本层找不到向外一层查找 【作用域链】
2. 注意：变量提升【悬挂声明】
3. 优先级
	声明变量 > 函数的声明 > 参数 > 变量提升
4. js没有块级作用域（除了函数）
```

​				面试题：JS对象考题

​				面试题：JS作用域+this指向+原型 考题

​				面试题：JS判断变量是不是数组，你能写出哪些方法？

​				面试题：slice是干嘛的、splice是否会改变原数组

​				面试题：JS数组去重

​				面试题：找出多维数组最大值

​				面试题：给字符串新增方法实现功能

```
String.prototype.adds = function( s ){
	return s + this;
}
console.log( '你好'.adds('hello') );
```

​				面试题：找出字符串出现最多次数的字符以及次数				

​		2.4 真正移动端 —— H5/C3面试题	

​				面试题：什么是语义化标签

​				面试题：::before 和 :after中双冒号和单冒号 有什么区别？解释一下这2个伪元素的作用。

```
伪类   :hover
伪元素 ::before、::after 
```

​				面试题：如何关闭iOS键盘首字母自动大写

​				面试题：怎么让Chrome支持小于12px 的文字？

```
div{
		font-size:10px;
}
p{
		display: inline-block;
		transform: scale(.1);
}
```

​				面试题：rem和em有什么样区别

```
rem针对于根(html)的font-size
em针对于父元素的font-size
```

​				面试题：ios系统中元素被触摸时产生的半透明灰色遮罩怎么去掉

​				面试题：webkit表单输入框placeholder的颜色值能改变吗？

​				面试题：禁止ios 长按时不触发系统的菜单，禁止ios&android长按时下载图片

​				面试题：禁止ios和android用户选中文字

​				面试题：自适应	[淘宝无线适配]

​				面试题：响应式

第三章 面试题进阶篇

​		3.1 JavaScript进阶面试题

​				面试题：new操作符具体做了什么

```
1. 会创建一个新对象   ：  返回对象
2. 原型赋值
3. 改变this指向
4. 判断构造函数最后返回的是什么类型
（如果是基本类型则无视，如果是引用类型则返回该对象，new不起作用了）
```

​				面试题：闭包  		【必须会】

```
无意间环境的共享  【不是作者设计的】

1. 什么是闭包或闭包是什么情况
	2个函数，这俩函数作用域是链接，内部函数可以访问外部函数的局部变量。
2. 闭包可以干什么事情？闭包的优点
	本身调用函数就会垃圾回收局部变量，但是因为是闭包现象所以不会回收。
	优点：外部函数的局部变量驻留在内存中，不会垃圾回收掉。
3. 闭包缺点。
	因为外部函数被调用完就应该垃圾回收，但是因为是闭包现象所以内部还可以访问外部函数的局部变量，因此外部函数的局部变量会驻留在内存中，导致性能会受到一些影响。
4. 闭包场景和如何解决缺点
	4.1 比如事件是异步【事件循环中，拿到的是同步执行最后的结果】，因为闭包是俩函数作用域链接，我可以在事件外部弄一个函数（同步），造成闭包现象，外部函数的局部变量就驻留在内存中，不会立即销毁了。
	4.2 如何解决缺点
		把闭包的函数设置为null。
```

​				面试题：原型链      【必须会】

```
1. 原型是干什么的？
		解决new不能对象的属性或者方法==》原型可以共享属性和方法
		
2. 谁有原型
	每一个函数都有prototype 【系统内置】
	每一个对象都有__proto__

3. 构造函数和构造出来的new对象有什么关系
	new 对象是构造函数实例出来的，构造函数的原型和new 对象的原型是同一个

4. 什么是原型链
	把原型连起来，形成一个原型的链条

5. 对象查找某个属性或者方法的规则（顺序）

	先在对象本身找==》构造函数中找===》对象原型中找==》构造函数的原型中找==》对象的原型的原型中找==》对象的原型的原型的原型中找....===》null （对象找不到属性或者方法返回的是undefined）

6. 原型链最顶端是null

***prototype（原型）==》属性 | 对象	
```

​				面试题： JS继承有哪些方式

```
一、es6继承
class Parent{
    constructor(){
      this.age = 19;
    }
}
class Child extends Parent{
	constructor(){
		super();
		this.name = '自傲三';
	}
}
var obj1 = new Child();
console.log( obj1.age );

二、原型链继承
function Parent(){
	this.age = 19;
	this.run = function(){}
}

function Child(){
	this.name = '张三'
}
//原型链
Child.prototype = new Parent();
var o1 = new Child();
var o2 = new Child();
console.log(  o1.run === o2.run );

三、借用构造函数的形式继承
function Parent(){
	this.age = 19;
	this.run = function(){}
}

function Child(){
	Parent.call(this);
	this.name = '张三'
}

var o1 = new Child();
var o2 = new Child();

console.log(  o1.run === o2.run );

```

​				面试题：说一下call、apply、bind区别

```
共同点：都是来改变this指向
	语法：函数.call 、 函数.apply 、 函数.bind
不同点：
	1. call和apply是立即执行的。bind返回的是一个函数体，需要()执行函数。
	2. apply第二个参数是数组，call、bind是多个参数。
场景：
	1. bind ：给dom添加一个事件，事件的赋值肯定是函数，这时候要改变this指向并且返回的函数体，必须使用bind
	2. apply ： 
			var arr = [1,4,4,545,3,5,435,3];
			console.log( Math.max.apply(this,arr) );
	3. 剩余情况用call
```

​				面试题：sort背后原理是什么？

​				面试题：深拷贝和浅拷贝

```
共同点：复制

1. 浅拷贝：复制引用，而不是真正的复制了值。
	某一个改变互相影响
	var arr1 = ['a','b']
	var arr2 = arr1;
	
	Object.assign()
	
2. 深拷贝：复制不是引用，复制了真正的值。
	改变互相不影响
	
	JSON.parse和自己封装
```

​				面试题：localstorage、sessionstorage、cookie的区别

```
共同点：
	localstorage、sessionstorage、cookie：存储在客户端
	seesion ：服务端
功能：
	localstorage、sessionstorage、cookie：一样【本地的存储】
区别：
	1. localstorage、cookie可以做到持久化存储，sessionstorage每次进入浏览器都是第一次（新值）
	2. cookie可以设置过期时间，localstorage、sessionstorage不可以设置过期时间
	3. 存储量大小 : 每个浏览器大小都是不同的
		localstorage、sessionstorage : 5MB
		cookie：4k
	4. cookie必须有环境才可以。【线上环境】
```

​		3.2 ES6面试题

​				面试题：var、let、const区别

```
相同点：都是来声明变量|常量
不同点：
  1. 变量提升
    var 有变量提升。
    let、const没有变量提升。
  2. 自身(变量)作用域
		var“没有”自身作用域
		let、const“有”自身作用域
	3. 声明同一个变量
		var 可以声明多个同一个变量名
		let 、const不可以
	4. let和const不同
		let 声明完可以再次赋值
		const 声明完就不可以再次赋值
		
***针对于const的面试题
const obj = {
	a:1
}
obj.a = 200;
console.log( obj.a, obj )  obj内部的属性和方法可以修改。
```

​				面试题：作用域考题

```
1. 作用域：先在本层找，本层找不到向外一层查找 【作用域链】
	注意let 和 const 有自身作用域
2. 注意：变量提升【悬挂声明】
	let和const没有提升
3. 优先级
	声明变量 > 函数的声明 > 参数 > 变量提升
4. js没有块级作用域（除了函数）
	注意let 和 const 有自身作用域
```

​				面试题：将下列对象进行合并

​				面试题：箭头函数和普通函数有什么区别？

```
1. this指向问题
	普通函数的this是在调用时决定的。
	箭头函数中的this是在定义时决定的，定义该箭头函数，函数中的this，指向于箭头函数的所在环境。	
	
	箭头函数的this是永远不能改变的。
	
2. 箭头函数不能new，普通函数可以new
3. 箭头函数没有原型，普通函数只要声明系统内置prototype
4. 箭头函数没有arguments
```

​				面试题：Promise有几种状态

```
1. 有三种状态：pending（进行中）、fulfilled（已成功）和rejected（已失败）。
2. Promise是来解决异步编程的（ 代码如果一直嵌套【死亡地狱】，易读性很差）
```

​				面试题：find和filter的区别       【大厂】

​				面试题：some和every的区别   【大厂】

​		3.3 webpack面试题

​				面试题：webpack插件

​		3.4 Git面试题

​				面试题：git常用命令

​				面试题：解决冲突

​				面试题：GitFlow

第四章 面试题框架篇

​		4.1 区分初中高级的 —— Vue面试题

​				面试题：Vue2.x 生命周期有哪些？

1.系统自带八个

```
 	beforeCreate() {}, //生命周期 - 创建之前
  created() {},  //生命周期 - 创建完成（可以访问当前this实例）
  beforeMount() {}, //生命周期 - 挂载之前
  mounted() {},  //生命周期 - 挂载完成（可以访问DOM元素）
  beforeUpdate() {}, //生命周期 - 更新之前
  updated() {}, //生命周期 - 更新之后
  beforeDestroy() {}, //生命周期 - 销毁之前
  destroyed() {}, //生命周期 - 销毁完成
```

2.当一旦进入到某个组件会执行哪些生命周期

```
 beforeCreate() {}, //生命周期 - 创建之前
 created() {},  //生命周期 - 创建完成（可以访问当前this实例）
 beforeMount() {}, //生命周期 - 挂载之前
 mounted() {},  //生命周期 - 挂载完成（可以访问DOM元素）
```

3.$el和$data在哪个阶段有

```
 beforeCreate() {},  啥也没有
 created() {},       有$data没有$el
 beforeMount() {},   有$data没有$el
 mounted() {},  		 有$data有$el
 
 $data就是数据 data 
 $el就是节点，本组件的根节点
```

4.如果使用keep-alive会多俩个生命周期

```
activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
deactivated() {},
```

5.如果加入keep-alive第一次进入组件会执行哪些生命周期

```
beforeCreate 
created 
beforeMount 
mounted 
activated
```

6.如果加入keep-alive第二次或者第N进入该组件会执行哪些生命周期

```
activated
```

​				面试题：谈谈你对keep-alive的了解

```
keep-alive ： 这是vue内置的一个组件，功能是来缓存组件的。
一旦使用了keep-alive会多俩个生命周期：
		activated() {}, //每次进入
		deactivated() {}, //销毁
```

​				面试题：v-if和v-show区别

```
一、创建和显示
	v-if 		创建和删除的操作      ===》重绘
	v-show  是隐藏和显示(display) ===》会造成回流和重绘
二、使用上
	v-show 初次加载“会”影响，切换比较频繁的时候用
	v-if   初次加载“不会”影响，不频繁切换用
```

​				面试题：v-if和v-for优先级 2.x

```
v-for 比 v-if高
```

​				面试题：ref是什么？

```
获取dom节点
```

​				面试题：nextTick是什么？

```
dom都加载完毕，会执行这里的代码
```

​				面试题：Vue中如何做样式穿透

```
>>>     【stylus】
/deep/  【sass、less】
::v-deep 【通用】
```

​				面试题：scoped原理

```
当组件的style使用了scoped，该组件中的所有dom节点会加入自定义属性data-v-xxx，css会匹配到h1[data-v-xxx]从而实现css局部化
说白了：就是css属性选择器
```

​				面试题：Vuex是单向数据流还是双向数据流？

```
单向数据流
```

​				面试题：讲一下MVVM

```
1. MVVM是来解决什么问题
	传统前后端分离不用MVVM框架，可能单个页面内容过多不好维护，而且操作dom太多了
	MVVM可以把单个页面分成好多组件，这样好维护，而且是数据驱动。
	
2. M（data）、V（视图template）、VM（vue源码：例如双向绑定）
```

​				面试题：双向绑定原理

```
1. 初始化的时候，把所有视图层的数据添加到对象中
2. 劫持数据发生的改变【哪个数据添加了v-model】
3. 劫持的数据去通知dep（订阅者）：具体知道哪个数据要改变
4. 订阅者通知waterch对象，触发update方法来更新视图层

补充：
data是响应式的，因为data的数据要赋值给new Vue这个实例，而且this.xxx改变data也会跟着改变，所以data是响应式的
```

​				面试题：什么是虚拟DOM

```
是什么：是数据、对象、就是把dom树转换成数据。
优点：提升性能
```

​				面试题：key是干什么？

```
key：是dom的唯一表示，key是可以提升性能的(如果节点的key不同，那么就会新建)。
```

​				面试题：diff算法

```
1. dom元素不同，永远都会新建。
2. diff如果不加入key，就没用了。如果key不同也是永远新建。
3. 同层比较

视频：https://www.bilibili.com/video/BV1K64y1s7ot?from=search&seid=5166436336620170103&spm_id_from=333.337.0.0
```

​				面试题：Vue组件传值

​				面试题：props和data优先级谁高？

```
Props ->  Methods ->  Data -> Computed -> Watch 
```

​				面试题：computed、methods、watch有什么区别？

```
1. computed有缓存，methods没缓存，watch[只要数据不变，就不会执行]
2. 一旦进入组件会执行 computed、methods
3. watch可以监听数据发生的改变（新老值），路由发生改变（新老路由）

***注意能扩展一下优先级是最好的了！
```

​				面试题：Vuex

```
1. vuex有哪些属性：state、getters、mutations、actions、modules
2. 为什么在组件中不能直接修改state或getters中的数据：因为vuex是单向数据流
	怎么改：通过mutations去修改
3. mutations 和 actions 区别
	mutations必须是同步函数、actions可以包含异步操作	
4. 使用
	actions是来提交mutations，尽量别直接在actions中写入方法
	mutations是来改变state数据的。
	如果是异步就放在actions中、同步放在mutations中

***注意：vuex 本身不能做持久化存储（刷新页面数据回到原点）。
解决：用localStorage或者vuex-persist插件。
```

​				面试题：Vue路由

```
1. Vue路由模式：history、hash
		hash样式是url带#，history不带#
		前端测试打包后组件内容空白，需要从history改成hash模式，当然如果正常上线，可能用history但是需要后端设置重定向来解决组件模块不显示的问题。
2. Vue路由导航守卫
	2.1 全局
		beforeEach()
		beforeResolve()
		afterEach()
	2.4 路由独享	
			beforeEnter()
	2.3 组件内
		beforeRouteEnter()
  	beforeRouteUpdate()
 	 	beforeRouteLeave()
3. 动态路由
	 场景：详情页(新闻、商品)
4. 路由传值
	this.$router.push({
		query:{a:1}
	})
	
	this.$router.push({
		params:{b:2}
	})
```

​				面试题：Vue项目打包后出现空白页

```
1. vue.config.js没有加入
	module.exports = {
 	 	publicPath:'./'
	}
2. 前端测试的时候：有路由没有页面数据。
	测试环节路由需要改成：hash模式
	上线用history，但是后端要做重定向
```

​		4.2 微信小程序面试题

​				面试题：如何自定义头部？

​				面试题：如何自定义底部？

​		4.3 uni-app面试题

​				面试题：生命周期

​				面试题：条件编译

第五章 面试题性能优化篇

```
性能优化最终目的：提升用户体验
项目优化阶段：
	开发阶段
	生产阶段：不断优化的过程
		借助工具测试
		npm install -g lighthouse
		lighthouse https://www.xuexiluxian.cn/
	
1. 首次加载如何提升性能：
	1.1 减少http请求  
		解决：合并数据
	1.2 script标签加入顺序
		解决：<script	defer> 或者 放在/body前面
	1.3 多个小图标使用雪碧图
	1.4 懒加载
	1.5 减少重绘和回流

2. 后端给你数据有10万条，你如何优化
	解决：长列表 （底部加载更多）

3. 项目上线前的性能优化
	压缩打包html、css、js、图片（base64）等等
```

第六章 面试题兼容篇

​		6.1 页面样式兼容 【移动端】

```
1. click事件在移动端有300ms延迟
	解决：<meta content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0" name="viewport">     
2. touch事件有穿透的问题
	解决：引入faskclick.js
	if ('addEventListener' in document) {
    document.addEventListener('DOMContentLoaded', function() {
      FastClick.attach(document.body);
    }, false);
  }
3. IOS键盘首字母自动大写
	解决：<input type="text" autocapitalize='off'> 
4. 在移动端修改难看的点击的高亮效果，iOS和安卓下都有效：
	解决：a,button,input{-webkit-tap-highlight-color:rgba(0,0,0,0);}
5. 在IOS中new date日期对象 new Date('2021-1-1')不显示
	解决：var date = new Date('2021/1/1');
```

​		6.2 框架兼容

```
uni-app 获取可视区域高
uni-app swiper固定高度
```

第七章 面试题网络请求篇

​		7.1 跨域面试题

```
1. vue中可以设置代理，来解决跨域.
	问题：但是打包以后，代理就失效了。
	解决：可以配置
				.env.development(开发环境)
				.env.production（生产环境）
2. 后端设置跨域(cors)
3. jsonp
```

​		7.2 http和https

```
正常一个网页是http，可以配置成https，而https就是一个证书（就是一个文件）。

1. https比http 更安全
2. 口端不同http:80 、https:443
```

第八章 WEB安全篇

​		8.1 XSS攻击

```
input正则限制不能输入特殊字符
&lg;  &gt; 字符集
```

​		8.2 SQL注入

```
input正则限制不能输入特殊字符
```

​		8.3 接口安全

```
1. 只是后端做
2. 前端做，后端也做
```

第九章 其他类面试题

​		9.1 token

​		9.2 SEO

```
1. 多页面
2. 数据不能是请求过来的。是直接在html中存在的：因为搜索引擎的蜘蛛要抓取
3. 网页title、描述、关键字
4. 页面标签合理使用 h1 、title 、属性:图片的===》alt
```

