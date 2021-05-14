# 第一章 JavaScript

## 1. 初识JavaScript

​    JavaScript 是什么

- 布兰登·艾奇（Brendan Eich，1961年～）。 
- 神奇的大哥用10天完成 JavaScript 设计。 
- 最初命名为 LiveScript，后来在与 Sun 合作之后将其改名为 JavaScript。
- JavaScript 是世界上最流行的语言之一，是一种运行在客户端的脚本语言 （Script 是脚本的意思） 



## 2.  JavaScript 的作用 

1. 表单动态校验（密码强度检测） （ JS 产生最初的目的 ） 
2. 网页特效 
3. 服务端开发(Node.js) 
4. 桌面程序(Electron) 
5. App(Cordova)  
6. 控制硬件-物联网(Ruff) 
7. 游戏开发(cocos2d-js)



## 3.  JS 的组成 

- ##### ECMAScript ：JavaScript语法 

  ECMAScript 规定了JS的编程语法和基础核心知识，是所有浏览器厂商共同遵守的一套JS语法工业标准。 

- ##### DOM ：页面文档对象模型  

  文档对象模型（Document Object Model，简称DOM），是W3C组织推荐的处理可扩展标记语言的标准编程接口。 通过 DOM 提供的接口可以对页面上的各种元素进行操作（大小、位置、颜色等）。

- ##### BOM ：浏览器对象模型

  BOM (Browser Object Model，简称BOM) 是指浏览器对象模型，它提供了独立于内容的、可以与浏览器窗口进行 。互动的对象结构。通过BOM可以操作浏览器窗口，比如弹出框、控制浏览器跳转、获取分辨率等。



## 4.  JS 有3种书写位置

分别为行内、内嵌和外部。 

行内：

```
<input type="button" value="点我试试" onclick="alert('Hello World')" /> 
```

**注意单双引号的使用：在HTML中我们推荐使用双引号, JS 中我们推荐使用单引号** 

 内嵌 ：

```
 <script> 

 alert('Hello World~!'); 

 </script>
```

外部 JS文件 

```
<script src="my.js"></script>
```

##  5.  JavaScript 输入输出语句 

```
alert(msg) 			 浏览器弹出警示框
console.log(msg) 	 浏览器控制台打印输出信息 
prompt(info)		浏览器弹出输入框，用户可以输入
```







# 第二章 变量

## 1.  声明变量 

1.同时声明多个变量时，只需要写一个 var， 多个变量名之间使用英文逗号隔开

2. 声明变量特殊情况

```
var age ; console.log (age);         只声明 不赋值                      undefined 

console.log(age)                     不声明 不赋值 直接使用     		  报错 

age = 10; console.log (age);       	 不声明 只赋值 		     		 10
```



## 2. 变量命名规范 

- 由字母(A-Za-z)、数字(0-9)、下划线(_)、美元符号( $ )组成，如：usrAge, num01, _name 
- 严格区分大小写。var app; 和 var App; 是两个变量 
- 不能 以数字开头。 18age 是错误的 
- 不能 是关键字、保留字。例如：var、for、while 
- 变量名必须有意义。 MMD BBD nl → age  
- 遵守驼峰命名法。首字母小写，后面单词的首字母需要大写。 myFirstName 
- 推荐翻译网站： 有道 爱词霸



## 3. 总结

1. ##### 为什么需要变量？ 

   因为我们一些数据需要保存，所以需要变量 

2. ##### 变量是什么？

   变量就是一个容器，用来存放数据的。方便我们以后使用里面的数据

3. ##### 变量的本质是什么? 

   变量是内存里的一块空间，用来存储数据

4. ##### 变量怎么使用的？ 

   我们使用变量的时候，一定要声明变量，然后赋值 

   声明变量本质是去内存申请空间 

5. ##### 什么是变量的初始化？ 

   声明变量并赋值我们称之为变量的初始化

6. ##### 变量命名规范有哪些？ 

   变量名尽量要规范，见名知意——驼峰命名法 

7. ##### 交换2个变量值的思路 

   区分哪些变量名不合法  

   学会交换2个变量





# 第三章  数据类型

## 1.  数据类型 

1. **简单数据类型** 

- Number

   isNaN()  用来判断一个变量是否为非数字的类型，返回 true 或者 false。

  ```
  var usrAge = 21; 
  
  var isOk = isNaN(userAge); 
  
  console.log(isNum); // false ，21 不是一个非数字 
  
  var usrName = "andy"; 
  
  console.log(isNaN(userName)); // true ，"andy"是一个非数字
  ```

  

- String 

   因为 HTML 标签里面的属性使用的是双引号，JS 这里我们更推荐使用单引号。 

  通过字符串的 length 属性可以获取整个字符串的长度。

  ```
  var strMsg = "我是帅气多金的程序猿！"; 
  
  alert(strMsg.length); // 显示 11
  ```

- Boolean

- Undefined

- Null  

**2.复杂数据类型** 

- object

**3.数值型三个特殊类型**

- Infinity ， 代表无穷大，      大于任何数值 
- -Infinity ，代表无穷小，     小于任何数值  
- NaN ，     Not a number，代表一个非数值



## 2.  获取数据类型 typeof 

可用来获取检测变量的数据类型 

```
var num = 18; 

console.log(typeof num) // 结果 number 

```



## 3.  数据类型转换

1. 转换为字符串

![1620031303479](C:\Users\ADMINI~1\AppData\Local\Temp\1620031303479.png)

2.  转换为数字型（重点）

![1620031482864](C:\Users\ADMINI~1\AppData\Local\Temp\1620031482864.png)

3. 转换为布尔型

![1620031636048](C:\Users\ADMINI~1\AppData\Local\Temp\1620031636048.png)

 

**扩展**

- Undefined 和 Null

1.一个声明后没有被赋值的变量会有一个默认值 undefined ( 如果进行相连或者相加时，注意结果） 

```
var variable; 

console.log(variable); // undefined 

console.log('你好' + variable); // 你好undefined 

console.log(11 + variable); // NaN 

console.log(true + variable); // NaN
```

2.一个声明变量给 null 值，里面存的值为空（学习对象时，我们继续研究null) 

```
var vari = null; 

console.log('你好' + vari); // 你好null 

console.log(11 + vari); // 11 

console.log(true + vari); // 1
```



-  关键字：是指 JS本身已经使用了的字，不能再用它们充当变量名、方法名。 

包括：break、case、catch、continue、default、delete、do、else、finally、for、function、if、in、 

instanceof、new、return、switch、this、throw、try、typeof、var、void、while、with 等。



- 保留字：实际上就是预留的“关键字”，意思是现在虽然还不是关键字，但是未来可能会成为关键字，同样不能 

使用它们当变量名或方法名。 

包括：boolean、byte、char、class、const、debugger、double、enum、export、extends、 

fimal、float、goto、implements、import、int、interface、long、mative、package、 

private、protected、public、short、static、super、synchronized、throws、transient、 

volatile 等





# 第四章  运算符

## 1.运算符

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200711174202675.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0ODY2MTUz,size_16,color_FFFFFF,t_70)





## 2.逻辑运算符

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200711174224580.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0ODY2MTUz,size_16,color_FFFFFF,t_70)



```
   // 1. 逻辑与 &&  and 两侧都为true  结果才是 true  只要有一侧为false  结果就为false 
        console.log(3 > 5 && 3 > 2); // false
        console.log(3 < 5 && 3 > 2); // true
        
   // 2. 逻辑或 || or  两侧都为false  结果才是假 false  只要有一侧为true  结果就是true
		console.log(3 > 5 || 3 > 2); // true 
		console.log(3 > 5 || 3 < 2); // false

   // 3. 逻辑非  not  ！ 
        console.log(!true); // false
```

 





# 第五章  函数

## 1. 函数的概念

就是封装了一段可被重复调用执行的代码块。通过此代码块可以实现大量代码的重复使用。 



## 2. 函数的使用

1.函数在使用时分为两步：声明函数和调用函数。 

![img](https://img-blog.csdnimg.cn/20200711213017803.png) 



## 3.  函数的参数

在函数内部某些值不能固定，我们可以通过参数在调用函数时传递不同的值进去。



## 4.  arguments 的使用  

- 只有函数才有 arguments对象 
- 而且是每个函数都内置好了这个arguments 
- 里面存储了所有传递过来的实参 

```
function fn() {

            // console.log(arguments); // 里面存储了所有传递过来的实参  arguments = [1,2,3]

            // console.log(arguments.length);

            // console.log(arguments[2]);

            // 我们可以按照数组的方式遍历arguments

            for (var i = 0; i < arguments.length; i++) {

                console.log(arguments[i]);
             }
        }

        fn(1, 2, 3);

        fn(1, 2, 3, 4, 5);
```

5.3.1  伪数组并不是真正意义上的数组

1. 具有数组的 length 属性

2. 按照索引的方式进行存储的

3. 它没有真正数组的一些方法 pop()  push() 等等



## 5.函数的案例

###    冒泡排序

```
  function sort(arr) {
           for (var i = 0; i < arr.length - 1; i++) {
               for (var j = 0; j < arr.length - i - 1; j++) {
                  if (arr[j] > arr[j + 1]) {
                      var temp = arr[j];
                       arr[j] = arr[j + 1];
                      arr[j + 1] = temp;
                  }
               }
           }
          return arr;
      }
       var arr1 = sort([1, 4, 2, 9]);
       console.log(arr1);
       var arr2 = sort([11, 7, 22, 999]);
       console.log(arr2);
```



# 第六章 作用域

## 1.作用域

通常来说，一段程序代码中所用到的名字并不是总是有效和可用的，而先定这个名字的可用性的代码范围就是这个名字的作用域。

作用域的使用提高了程序逻辑的局部性，增强了程序的可靠性，减少了名字的冲突。

1.JavaScript作用域 ： 就是代码名字（变量）在某个范围内起作用和效果 目的是为了提高程序的可靠性更重要的是减少命名冲突

2.js的作用域（es6）之前 ： 全局作用域   局部作用域 

3.全局作用域： 整个script标签 或者是一个单独的js文件

```
       var num = 10;
       var num = 30;
       console.log(num);
```

4. 局部作用域（函数作用域） 在函数内部就是局部作用域 这个代码的名字只在函数内部起效果和作用

```
       function fn() {
           // 局部作用域
           var num = 20;
           console.log(num);
        }
       fn();
```



## 2.变量的作用域

全局作用域 、局部作用域

1. 从执行效率来看全局变量和局部变量

  (1) 全局变量只有浏览器关闭的时候才会销毁，比较占内存资源

  (2) 局部变量 当我们程序执行完毕就会销毁， 比较节约内存资源



## 3.作用域链

作用域链  ： 内部函数访问外部函数的变量，采取的是链式查找的方式来决定取那个值 ，这种结构我们称为作用域链  ，就近原则 

```
        var num = 10;

        function fn() { // 外部函数
            var num = 20;
            
            function fun() { // 内部函数
                console.log(num);//20
            }
            
            fun();
        }
        fn();
```







# 第七章  预解析

## 1.预解析

js引擎运行js 分为两步： 预解析、 代码执行

 (1). 预解析： js引擎会把js 里面所有的 var  还有 function 提升到当前作用域的最前面

 (2). 代码执行 ： 按照代码书写的顺序从上往下执行



## 2.变量预解析和函数预解析

预解析分为：变量预解析（变量提升） 和 函数预解析（函数提升）

 (1) 变量提升： 就是把所有的变量声明提升到当前的作用域最前面  不提升赋值操作

 (2) 函数提升： 就是把所有的函数声明提升到当前作用域的最前面  不调用函数



# 第八章 对象

## 1.对象

1. 对象是一个具体的事物。

2. 在JS中，对象是一组无序的相关属性和方法的集合，所有的事物都是对象，例如：字符串、数值、数组、函数等。

3. 对象是由**属性**和**方法**组成的。

4. 属性：事物的特性，在对象中用属性来表示。

5. 方法：事物的行为，在对象中用方法来表示。

6. 为什么需要对象？

   保存一个值时，可以使变量；

   保存多个值（一组值）时，可以使用数组；

   保存一个人的完整信息可以用对象，表达结构更清晰，更强大。

   

## 2.创建对象的三种方式

1.利用字面量创建对象

```
 // var obj = {};  // 创建了一个空的对象 
        var obj = {
                uname: '张三疯',
                age: 18,
                sex: '男',
                sayHi: function() {
                    console.log('hi~');
                }
            }
```

2.利用new Object创建对象

```
  // 利用 new Object 创建对象
        var obj = new Object(); // 创建了一个空的对象
        obj.uname = '张三疯';
        obj.age = 18;
        obj.sex = '男';
        obj.sayHi = function() {
                console.log('hi~');

            }
```

3.利用构造函数创建对象

```
  function Star(uname, age, sex) {
            this.name = uname;
            this.age = age;
            this.sex = sex;
            this.sing = function(sang) {
                console.log(sang);
            }
        }
```



## 3. new关键字

执行过程

1. new 构造函数可以在内存中创建了一个空的对象 
2. this 就会指向刚才创建的空对象
3. 执行构造函数里面的代码 给这个空对象添加属性和方法
4.  返回这个对象



## 4. 遍历对象

使用 for in 里面的变量 我们喜欢写 k  或者  key 

```
var obj = {
           name: 'pink老师',
            age: 18,
           sex: '男',
           fn: function() {}
          }
         // console.log(obj.name);
         // console.log(obj.age);
         // console.log(obj.sex);
         // for in 遍历我们的对象
         // for (变量 in 对象) {
 } 
for (var k in obj) {
		console.log(k); // k 变量 输出  得到的是 属性名
	     console.log(obj[k]); // obj[k] 得到是 属性值
 }
```



# 第九章 JavaScript内置对象

## 1. 内置对象

1.JavaScript 中的对象分为3种：自定义对象、内置对象、浏览器对象

2.前面两种对象是JS基础内容，属于ECMAScript；第三个浏览器对象属于我们JS独有的。

3.内置对象就是指JS语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本而必要的功能。

4.内置对象最大的优点就是帮助我们快速开发。

5.JavaScript提供了对各内置对象：Math、Data、Arrary、String



## 2. 查文档

- MDN

- W3C

  

## 3. Math对象

1.Math数学对象不是一个构造函数 ，所以我们不需要new 来调用 而是直接使用里面的属性和方法即可 。

```
 	    console.log(Math.PI); // 一个属性 圆周率
        console.log(Math.max(1, 99, 3)); // 99
        console.log(Math.max(-1, -10)); // -1
        console.log(Math.max(1, 99, 'pink老师')); // NaN
        console.log(Math.max()); // -Infinity
```

2.random获取随机数

```
		console.log(Math.random()); 
```

3.绝对值

```
        console.log(Math.abs(1)); // 1
        console.log(Math.abs(-1)); // 1
        console.log(Math.abs('-1')); // 隐式转换 会把字符串型 -1 转换为数字型
        console.log(Math.abs('pink')); // NaN 
```

4. 取整

（1）.Math.floor()   地板 向下取整  往最小了取值

```
	 console.log(Math.floor(1.1)); // 1
 	 console.log(Math.floor(1.9)); // 1
```

（2）.Math.ceil()    ceil 天花板 向上取整  往最大了取值

```
        console.log(Math.ceil(1.1)); // 2
        console.log(Math.ceil(1.9)); // 2
```

（3）.Math.round()   四舍五入  其他数字都是四舍五入，但是 .5 特殊 它往大了取  

```
        console.log(Math.round(1.1)); // 1
        console.log(Math.round(1.5)); // 2
        console.log(Math.round(1.9)); // 2
        console.log(Math.round(-1.1)); // -1
        console.log(Math.round(-1.5)); // 这个结果是 -1
```



## 4. Date对象

 Date() 日期对象是一个构造函数 必须使用new 来调用创建我们的日期对象 。

1.使用Date， 如果没有参数，返回当前系统的当前时间 。

```
 	 var date = new Date();
     console.log(date);
```

2.参数常用的写法 ：数字型  2019, 10, 01  或者是 字符串型 '2019-10-1 8:8:8' 

```
   var date1 = new Date(2019, 10, 1);
   console.log(date1); // 返回的是 11月 不是 10月 
   var date2 = new Date('2019-10-1 8:8:8');
   console.log(date2);
```

3.获取年月日星期。

```
 	    var date = new Date();
        console.log(date.getFullYear()); // 返回当前日期的年  2019
        console.log(date.getMonth() + 1); // 月份 返回的月份小1个月   记得月份+1 呦
        console.log(date.getDate()); // 返回的是 几号
        console.log(date.getDay()); // 3  周一返回的是 1 周六返回的是 6 但是 周日返回的是 0
```

4.获取时分秒。

```
        var date = new Date();
        console.log(date.getHours()); // 时
        console.log(date.getMinutes()); // 分
        console.log(date.getSeconds()); // 秒
```

5.封装一个函数返回当前的时分秒 格式 08:08:08 

```
function getTimer() {
            var time = new Date();
            var h = time.getHours();
            h = h < 10 ? '0' + h : h;
            var m = time.getMinutes();
            m = m < 10 ? '0' + m : m;
            var s = time.getSeconds();
            s = s < 10 ? '0' + s : s;
            return h + ':' + m + ':' + s;
        }
        console.log(getTimer());
```



## 5. 数组对象

**增删改查数组**

1.push() 在我们数组的末尾 添加一个或者多个数组元素   push  推 

```
 		var arr = [1, 2, 3];
        // arr.push(4, 'pink');
        console.log(arr.push(4, 'pink'));
```

2.unshift()在我们数组的开头 添加一个或者多个数组元素 

```
 console.log(arr.unshift('red', 'purple'));
```

3.pop() 它可以删除数组的最后一个元素   

```
 console.log(arr.pop());
```

4.shift() 它可以删除数组的第一个元素   

```
console.log(arr.shift());
```

5.indexOf(数组元素) :返回数组元素索引号方法 

- 作用:返回该数组元素的索引号 

- 从前面开始查找

- 它只返回第一个满足条件的索引号 

- 它如果在该数组里面找不到元素，则返回的是 -1  


```
  var arr = ['red', 'green', 'pink'];
  console.log(arr.indexOf('blue'));//-1
```

-  返回数组元素索引号方法  lastIndexOf(数组元素)  作用就是返回该数组元素的索引号 从后面开始查找

```
   var arr = ['red', 'green', 'blue', 'pink', 'blue'];
   console.log(arr.lastIndexOf('blue')); // 4
```

6.str.indexOf('要查找的字符', [起始的位置])

```
  		var str = '改革春风吹满地，春天来了';
        console.log(str.indexOf('春'));//2
        console.log(str.indexOf('春', 3)); // 从索引号是 3的位置开始往后查找 //8
```

7.charAt() 根据位置返回字符 

```
 	    var str = 'andy';
        console.log(str.charAt(3));
```

8.charCodeAt(index)  返回相应索引号的字符ASCII值 目的： 判断用户按下了那个键  

```
 console.log(str.charCodeAt(0)); // 97
```

9.join() 分隔符

```
	    var arr1 = ['green', 'blue', 'pink'];
        console.log(arr1.join()); // green,blue,pink
        console.log(arr1.join('-')); // green-blue-pink
        console.log(arr1.join('&')); // green&blue&pink
```

 



## 6.字符串对象

1. concat('字符串1','字符串2'....)

```
		var str = 'andy';
	    console.log(str.concat('red'));
```

  2. substr('截取的起始位置', '截取几个字符');  

```
 	var str1 = '改革春风吹满地';
	 console.log(str1.substr(2, 2)); // 第一个2 是索引号的2 从第几个开始  第二个2 是取几个字符
```





# 第十章 Web APIs

## 1. Web APIs和JS基础关联性

1.JavaScript 的组成：

- ECMAScript(JavaScript 语法，JavaScript 基础)
- DOM页面文档对象模型（Web APIs）
- BOM浏览器对象模型（Web APIs）



## 2. API和Web APIs

1.API：是一些预先定义的函数，目的是提供应用程序与开发人员基于某软件或者硬件得以访问一组列程的能力，而又无序访问源码，或理解内部工作机制的细节。

2.简单理解：API是给程序员提供的一种格局，以便更轻松的实现想要完成的功能。

3.Web API ：是浏览器提供的一套操作浏览器功能和页面元素的API(DOM和BOM).

4.Web API主要是针对于浏览器提供的接口，主要针对于浏览器做交互效果。

5.Web API一般都有输入和输出（函数的传参和返回值），Web API很多都是方法（函数）。







# 第十一章 DOM

## 1. DOM简介

1. DOM:文档对象模型，通过DOM接口可以改变我也的内容、结构和样式。
2. 文档：一个页面就是一个文档，DOM中使用document表示。
3. 元素：页面中的所有标签都是元素，DOM中使用element表示。
4. 节点：网页中的所有内容都是节点（标签、属性、文本、注释等），DOM中使用node表示。



## 2.  获取元素

1. getElementById 获取元素，返回的是一个元素对象 

   ```
           var timer = document.getElementById('time');
           console.log(timer);
           console.log(typeof timer);
   ```

2. getElementsByTagName 获取元素，获取过来元素对象的集合 以伪数组的形式存储的 

   ```
   <ul>
           <li>知否知否，应是等你好久11</li>
           <li>知否知否，应是等你好久11</li>
           <li>知否知否，应是等你好久11</li>
           <li>知否知否，应是等你好久11</li>
   </ul>
   		 var lis = document.getElementsByTagName('li');
           console.log(lis);
           console.log(lis[0]);
   ```

   **父元素必须是指定的单个元素**

   ```
   <ol id="ol">
           <li>生僻字</li>
           <li>生僻字</li>
           <li>生僻字</li>
           <li>生僻字</li>
   
   </ol>
   		 var ol = document.getElementById('ol');
           console.log(ol.getElementsByTagName('li'));
   ```

3. （H5新增）getElementsByClassName 获取元素，根据类名获得某些元素集合 

   ```
   	    var boxs = document.getElementsByClassName('box');
           console.log(boxs);
   ```

4. （H5新增） querySelector 返回指定选择器的第一个元素对象  切记 里面的选择器需要加符号 .box  #nav 

   ```
   	    var firstBox = document.querySelector('.box');
           console.log(firstBox);
           var nav = document.querySelector('#nav');
           console.log(nav);
           var li = document.querySelector('li');
           console.log(li);
   ```

5. （H5新增）querySelectorAll()返回指定选择器的所有元素对象集合 

   ```
   		 var allBox = document.querySelectorAll('.box');
           console.log(allBox);
           var lis = document.querySelectorAll('li');
           console.log(lis);	
   ```

6. 获取body元素

   ```
    	    var bodyEle = document.body;
           console.log(bodyEle);
           console.dir(bodyEle);
   ```

7. 获取html元素

   ```
   	    var htmlEle = document.documentElement;
           console.log(htmlEle);	
   ```

   

## 3.  事件基础

1. 事件三要素：事件是有三部分组成  事件源  事件类型  事件处理程序   我们也称为事件三要素

```
      //(1) 事件源 事件被触发的对象   谁  按钮
      var btn = document.getElementById('btn');
      //(2) 事件类型  如何触发 什么事件 比如鼠标点击(onclick) 还是鼠标经过 还是键盘按下
      //(3) 事件处理程序  通过一个函数赋值的方式 完成
       btn.onclick = function() {
            alert('点秋香');
        }
```

2.执行事件步骤

  点击div 控制台输出 我被选中了

```
        // 1. 获取事件源

        var div = document.querySelector('div');

        // 2.绑定事件 注册事件

        // div.onclick 

        // 3.添加事件处理程序 

        div.onclick = function() {

            console.log('我被选中了');

 }

```



## 4.操作元素

1.innerText ：不识别html标签 非标准  去除空格和换行 

```
div.innerText = '<strong>今天是：</strong> 2019';
```

  //<strong>今天是：</strong> 2019

2.innerHTML：识别html标签 W3C标准 保留空格和换行的 

  div.innerHTML = '<strong>今天是：</strong> 2019';

   //**今天是：** 2019

3.自定义属性操作

   **获取元素属性**

   (1).getAttribute ().get得到获取 attribute 属性的意思 我们程序员自己添加的属性我们称为自定义属性 index 

```
<div id="demo" index="1" class="nav"></div>
        console.log(div.getAttribute('id'));
        console.log(div.getAttribute('index'));
```

(2)H5新增获取方法：h5新增的获取自定义属性的方法 它只能获取data-开头的 

```
        console.log(div.dataset);
        console.log(div.dataset.index);
        console.log(div.dataset['index']);
        // 如果自定义属性里面有多个-链接的单词，我们获取的时候采取 驼峰命名法
        console.log(div.dataset.listName);
        console.log(div.dataset['listName']);
```

4..设置元素属性值

(1) element.属性= '值'

```
        div.id = 'test';
        div.className = 'navs';
```

(2) element.setAttribute('属性', '值');  主要针对于自定义属性

```
        div.setAttribute('index', 2);
        div.setAttribute('class', 'footer'); // class 特殊  这里面写的就是class 不是className
```

3.移除属性 removeAttribute(属性)

```
     div.removeAttribute('index');
```

​    

## 5.  节点操作

1.父节点 parentNode ：得到的是离元素最近的父级节点(亲爸爸) 如果找不到父节点就返回为 null

```
        console.log(erweima.parentNode);
```

2.子节点

（1） 子节点  childNodes 所有的子节点 包含 元素节点 文本节点等等 

```
	    console.log(ul.childNodes);
```

（2） children 获取所有的子元素节点 也是我们实际开发常用的

```
        console.log(ul.children);
```

 (3) firstChild 第一个子节点 不管是文本节点还是元素节点

```
    	 console.log(ol.firstChild);
         console.log(ol.lastChild);

```

 (4). firstElementChild 返回第一个子元素节点 ie9才支持

```
		console.log(ol.firstElementChild);
	     console.log(ol.lastElementChild);
```

(5)实际开发的写法  既没有兼容性问题又返回第一个子元素

```
        console.log(ol.children[0]);
        console.log(ol.children[ol.children.length - 1]);

```

(6) nextSibling 下一个兄弟节点 包含元素节点或者 文本节点等等

```
        console.log(div.nextSibling);
	    console.log(div.previousSibling);
```

(7) nextElementSibling 得到下一个兄弟元素节点

```
		console.log(div.nextElementSibling);
		console.log(div.previousElementSibling);
```

3.创建节点元素节点

```
		var li = document.createElement('li');
```

4.添加节点 node.appendChild(child) 

  node 父级  

  child 是子级 后面追加元素  类似于数组中的push

```
 		var ul = document.querySelector('ul');
         ul.appendChild(li)
```

5.添加节点 node.insertBefore(child, 指定元素);

```
		var lili = document.createElement('li');
		 ul.insertBefore(lili, ul.children[0]);
```

6.删除节点 removeChild 

```
 ul.removeChild(ul.children[0]);//
```

7.克隆节点

(1) node.cloneNode(); 括号为空或者里面是false 浅拷贝 只复制标签不复制里面的内容

(2) node.cloneNode(true); 括号为true 深拷贝 复制标签复制里面的内容

```
     var lili = ul.children[0].cloneNode(true);
        ul.appendChild(lili);
```

8.document.write() 创建元素  如果页面文档流加载完毕，再调用这句话会导致页面重绘 

```
   var btn = document.querySelector('button');
        btn.onclick = function () {
            document.write('<div>123</div>');
        }
```

9.innerHTML 创建元素

```
 var inner = document.querySelector('.inner');

        for (var i = 0; i <= 5; i++) {

            inner.innerHTML += '百度' + '</br>'

        }

```

10. document.createElement() 创建元素

```
 var create = document.querySelector('.create');

        for (var i = 0; i <= 100; i++) {

            var a = document.createElement('a');

            create.appendChild(a);

```







# 第十二章 事件高级

## 1. 注册事件（绑定事件）

注册事件有两种方式：传统方式和方法监听注册方式。

1.传统方式注册事件，利用on

```
      var btns = document.querySelectorAll('button');
        // 1. 传统方式注册事件
        btns[0].onclick = function () {
            alert('hi');
        }
        btns[0].onclick = function () {
            alert('hao a u');
        }
```

2.事件监听注册addEventListener

-   里面的事件类型是字符串 必定加引号 而且不带on
-   同一个元素 同一个事件可以添加多个侦听器（事件处理程序）

```
        btns[1].addEventListener('click', function () {
            alert(22);
        })
        btns[1].addEventListener('click', function () {
            alert(33);
        })
```

3.attachEvent ie9以前的版本支持

```
btns[2].attachEvent('onclick', function() {
            alert(11);
        })
```



## 2. 删除事件（解绑事件）

1.传统删除事件

```
var divs = document.querySelectorAll('div');
        divs[0].onclick = function() {
                alert(11);
                divs[0].onclick = null;
            }


```

2.removeEventListener 删除事件      

```
divs[1].addEventListener('click', fn) // 里面的fn 不需要调用加小括号
function fn() {
            alert(22);
            divs[1].removeEventListener('click', fn);
        }

```

3.detachEvent删除事件

```
 divs[2].attachEvent('onclick', fn1);
        function fn1() {
            alert(33);
            divs[2].detachEvent('onclick', fn1);
        }

```

 

## 3. DOM事件流

1.事件流描述的是从页面中接收事件的顺序。

2.事件发生会在元素节点之间按照特定的顺序传播，这个传播过程即DOM事件流。

3.DOM事件流分为三个阶段

-  JS 代码中只能执行捕获或者冒泡其中的一个阶段。
- onclick 和 attachEvent（ie） 只能得到冒泡阶段。

（1）捕获阶段：由DOM最 顶层节点开始，然后逐级向下传播到最具体的元素接收的过程。

- ​    如果addEventListener 第三个参数是 true ，那么则处于捕获阶段  
-    document -> html -> body -> father -> son

```
        var son = document.querySelector('.son');
        son.addEventListener('click', function() {
            alert('son');
        }, true);
        var father = document.querySelector('.father');
        father.addEventListener('click', function() {
            alert('father');
        }, true);
        //先弹出father
```

（2）当前目标阶段

（3）冒泡阶段：事件开始时由最具体的元素接收，然后逐级向上传播到DOM最顶层节点的过程。

-   如果addEventListener 第三个参数是 false 或者 省略 ，那么则处于冒泡阶段  
-  son -> father ->body -> html -> document

```
 var son = document.querySelector('.son');
        son.addEventListener('click', function() {
            alert('son');
        }, false);
        var father = document.querySelector('.father');
        father.addEventListener('click', function() {
            alert('father');
        }, false);
        document.addEventListener('click', function() {
            alert('document');
        })
        //son、father、document
```



## 4. 事件对象

1.e.target 返回的是触发事件的对象（元素） 

2.this 返回的是绑定事件的对象（元素） 

```
    <div>123</div>
    <ul>
        <li>abc</li>
        <li>abc</li>
        <li>abc</li>
    </ul>
```

```
  var ul = document.querySelector('ul');
        ul.addEventListener('click', function(e) {
         // 我们给ul 绑定了事件  那么this 就指向ul  
                console.log(this);
                console.log(e.currentTarget);

         // e.target 指向我们点击的那个对象 谁触发了这个事件 我们点击的是li e.target 指向的就是li
                console.log(e.target);
            })
```




## 5. 阻止事件冒泡

1.返回事件类型

```
        var div = document.querySelector('div');

        div.addEventListener('click', fn);//click

        div.addEventListener('mouseover', fn);//mouseover

        div.addEventListener('mouseout', fn);//mouseout
        
        function fn(e) {
            console.log(e.type);
        }
```

2.preventDefault阻止默认行为（事件）, 让链接不跳转, 或者让提交按钮不提交 

```
  var a = document.querySelector('a');
        a.addEventListener('click', function(e) {
                e.preventDefault(); //  dom 标准写法
            })
            
```

3.return false 也能阻止默认行为 没有兼容性问题

​    特点： return 后面的代码不执行了， 而且只限于传统的注册方式onclick.

```
        a.onclick = function(e) {
        
            // 普通浏览器 e.preventDefault();  方法
             e.preventDefault();
            
            // 低版本浏览器 ie678  returnValue  属性
             e.returnValue;
               
            return false;
            
            alert(11);
        }

```

4.阻止冒泡  (dom 推荐的标准) stopPropagation() 

```
 var son = document.querySelector('.son');

        son.addEventListener('click', function(e) {

            alert('son');

            e.stopPropagation();  // stop 停止  Propagation 传播

            e.cancelBubble = true; // 非标准 cancel 取消 bubble 泡泡

        }, false);

 

        var father = document.querySelector('.father');

        father.addEventListener('click', function() {

            alert('father');

        }, false);

        document.addEventListener('click', function() {

            alert('document');

        })

```

​       

## 6.事件委托（代理、委派）

1.事件委托的核心原理：给父节点添加侦听器， 利用事件冒泡影响每一个子节点

```
    var ul = document.querySelector('ul');

        ul.addEventListener('click', function(e) {

            // alert('知否知否，点我应有弹框在手！');

            // e.target 这个可以得到我们点击的对象

            e.target.style.backgroundColor = 'pink';
```

  

## 7.常用的鼠标事件

1.contextmenu 禁用右键菜单

```
document.addEventListener('contextmenu', function(e) {

                e.preventDefault();

            })
```

 2.selectstart禁止选中文字 

```
document.addEventListener('selectstart', function(e) {

            e.preventDefault();

        })


```

4.鼠标事件对象 MouseEvent

(1)client 鼠标在可视区的x和y坐标

```
   document.addEventListener('click', function(e) {

            console.log(e.clientX);

            console.log(e.clientY);

            console.log('---------------------');
```

(2) page 鼠标在页面文档的x和y坐标

```
 document.addEventListener('click', function(e) {
 
		   console.log(e.pageX);

            console.log(e.pageY);

            console.log('---------------------');
```

(3) screen 鼠标在电脑屏幕的x和y坐标

```
 document.addEventListener('click', function(e) {
 
		   console.log(e.screenX);

            console.log(e.screenY);

        })

```

5.跟随鼠标的天使

   核心原理： 每次鼠标移动，我们都会获得最新的鼠标坐标， 把这个x和y坐标做为图片的top和left 值就可以移动图片

```
<style>
        img {
            position: absolute;
            top: 2px;
        }
</style>
```

```
 <img src="images/angel.gif" alt="">
```

```
 <script>
        var pic = document.querySelector('img');
        document.addEventListener('mousemove', function(e) {
            //  mousemove只要我们鼠标移动1px 就会触发这个事件
           
            var x = e.pageX;
            var y = e.pageY;
            console.log('x坐标是' + x, 'y坐标是' + y);
           
           // 千万不要忘记给left 和top 添加px 单位
            pic.style.left = x - 50 + 'px';
            pic.style.top = y - 40 + 'px';

        });
    </script>
```



## 8.常用的键盘事件

1.键盘事件 keyup 、keypress、keydown

```
        document.addEventListener('keyup', function() {
            console.log('我弹起了');
        })

        //3. keypress 按键按下的时候触发  不能识别功能键 比如 ctrl shift 左右箭头啊
        document.addEventListener('keypress', function() {
                console.log('我按下了press');
            })
            
         //2. keydown 按键按下的时候触发  能识别功能键 比如 ctrl shift 左右箭头啊
        document.addEventListener('keydown', function() {
                console.log('我按下了down');
            })
       
       // 4. 三个事件的执行顺序  keydown -- keypress -- keyup
```



2.键盘事件对象中的keyCode属性可以得到相应键的ASCII码值

- 我们的keyup 和keydown事件不区分字母大小写  a 和 A 得到的都是65
-  我们的keypress 事件 区分字母大小写  a  97 和 A 得到的是65



# 第十三章 BOM

## 1.BOM概述

1.BOM是浏览器对象模型，他提供了独立于内容与浏览器窗口进行交互的对象，其核心对象是window。

2.BOM由一些列相关的对象构成，并且每个对象都提供了很多方法和属性。

3.BOM缺乏标准，JS语法的标准化组织是ECMA，DOM的标准化组织是W3C，BOM最初是Netscape浏览器标准的一部分。

4.DOM和BOM

DOM:

> 文档对象模型 
>
> DOM 就是把「文档」当做一个「对象」来看待 
>
> DOM 的顶级对象是 document
>
>  DOM 主要学习的是操作页面元素 
>
> DOM 是 W3C 标准规范 

BOM

> 浏览器对象模型 把「浏览器」当做一个「对象」来看待
>
>  BOM 的顶级对象是 window 
>
> BOM 学习的是浏览器窗口交互的一些对象
>
> BOM 是浏览器厂商在各自浏览器上定义的，兼容性较差 

## 2.window对象的常见事件

1.window 对象是浏览器的顶级对象，他具有双重角色。

- 它是JS访问浏览器窗口的一个接口。
- 他是一个全局对象。定义在全局作用域中的变量、函数都会变成window对象的属性和方法。
- 在调用的时候可以省略window，前面学习的对话框都属于window对象方法，如alert()、prompt()等。

2. window.onload是窗口(页面)加载事件，当文档内容完全加载完成会触发该事件（包括图像、脚本文件、CSS文件等），就调用的处理函数。

```
        window.onload = function() {
            var btn = document.querySelector('button');
            btn.addEventListener('click', function() {
                alert('点击我');
            })
        }
```

- 有了window.onload就可以把JS代码写到页面元素的上方，因为onload是等页面内容全部加载完毕再去执行处理函数。

- window.onload传统注册事件方式只能写一次，如果有多个，会以最后一个window.onload为准。

- 如果使用了addEventListener则没有限制。

  ```
          window.addEventListener('load', function() {
  
              alert(22);
          })
  ```

- DOMContentLoaded事件触发时，仅当DOM加载完成，不包括样式表，图片，flash等等。
- 如果页面的图片很多的话，从用户访问到onload触发可能需要较长的时间，交互效果就不能实现，必然影响用户的体验，此时用 DOMContentLoaded 事件比较合适。

```
        document.addEventListener('DOMContentLoaded', function() {
                alert(33);
            })
```

3.调整窗口大小事件

- winodw.onresize 是调整窗口大小加载事件，当触发时就调用的处理函数。
- 只要窗口大小发生像素变化，就会触发这个事件。
- 我们经常利用这个事件完成响应式布局。winodw.innerWidth当前屏幕的宽度。

```
        window.addEventListener('load', function() {
            var div = document.querySelector('div');
            window.addEventListener('resize', function() {
                console.log(window.innerWidth);

                console.log('变化了');
                if (window.innerWidth <= 800) {
                    div.style.display = 'none';
                } else {
                    div.style.display = 'block';
                }

            })
        })
```



## 3.定时器

12.setTimeout 

- 语法规范：  window.setTimeout(调用函数, 延时时间);
- 单位：毫秒，可以省略，如果省略默认的是0  

```
       setTimeout(function() {
            console.log('时间到了');
        }, 2000);

```

```
       function callback() {
            console.log('爆炸了');

        }
        var timer1 = setTimeout(callback, 3000);
        var timer2 = setTimeout(callback, 5000);

```

1.5秒后自动关闭

```
        var ad = document.querySelector('.ad');
        setTimeout(function() {
            ad.style.display = 'none';
        }, 5000);

```

2.清除延时时间，clearTimeout

```
        var btn = document.querySelector('button');
        var timer = setTimeout(function() {
            console.log('爆炸了');

        }, 5000);
        btn.addEventListener('click', function() {
            clearTimeout(timer);
        })

```

3.setInterval  :每隔这个延时时间，就去调用这个回调函数，会调用很多次，重复调用这个函数

```
        setInterval(function() {
            console.log('继续输出');
        }, 1000);


```

4.setTimeout 与 setInterval区别

- setTimeout  延时时间到了，就去调用这个回调函数，只调用一次 就结束了这个定时器
- setInterval  每隔这个延时时间，就去调用这个回调函数，会调用很多次，重复调用这个函数

5.this 指向问题

 一般情况下this的最终指向的是那个调用它的对象

 （1）**全局作用域**或者**普通函数**中this指向全局对象window（ 注意定时器里面的this指向window）

```
  console.log(this);
  //Window


```

```
 function fn() {
     console.log(this);
        }     
   window.fn();
  //Window


```

```
  window.setTimeout(function() {
            console.log(this);
        }, 1000);
   //Window


```

（2）方法调用中谁调用this指向谁

```
     var o = {
            sayHi: function() {
            console.log(this); // this指向的是 o 这个对象
            }
        }
        o.sayHi();
	 //Object


```

```
  var btn = document.querySelector('button');
        // btn.onclick = function() {
        //     console.log(this); // this指向的是btn这个按钮对象
        // }

        btn.addEventListener('click', function() {
                console.log(this); // this指向的是btn这个按钮对象
            })


```

（3）构造函数中this指向构造函数的实例

```
       function Fun() {
            console.log(this); // this 指向的是fun 实例对象
        }
        var fun = new Fun();


```

 

## 4.JS执行机制

1.JS是单线程

JavaScript语言的一大特点就是单线程，也就是说，同一个事件只能做一件事。这是因为JavaScript这门脚本语言诞生的使命所致-----JavaScript是为处理页面中用户的交互，以及操作DOM而诞生。比如我们对某个DOM元素进行添加和删除操作，不能同时进行。应该先进行添加，之后再删除。

2.同步任务：同步任务都在主线程上执行，形成一个执行栈。

3.异步任务是通过回调函数实现的，异步任务有三种类型：

（1）普通事件，如click、resize等；

（2）资源加载，如load、error等；

（3）定时器，包括setinterval、setTimeout等。

4.JS的执行机制：

（1）先执行执行栈中的同步任务；

（2）异步任务（回调函数）放入任务队列中；

（3）一旦执行栈中的所有同步任务执行完毕，系统就会按次序读取任务队列中的异步任务，于是被读取的异步任务结束等待状态，进入执行栈，开始执行。





## 5.location对象

1.window 对象给我们提供了一个location属性用于获取或设置窗体的URL，并且可以用于解析URL。因为这个属性返回的是一个对象，所以我们将这个属性也称为location对象。

2.location对象的属性

- location.href 		获取或者设置整个URL
- location.host                返回主机（域名）
- location.port                返回端口号，如果未写返回空字符
- location.pathname     返回路径
- location.search            返回参数
- location.hash               返回片段 

3.location对象的方法

- location.assign            跟href一样，可以跳转页面（也称为重定向页面）
- location.replace           替换当前页面，因为不记录历史，所以不能后退页面
- location.reload             重新加载页面，相当于刷新按钮或者f5 如果参数为 true 强制刷新 ctrl+f5

2.案例：5秒后跳转

```
        var btn = document.querySelector('button');
        var div = document.querySelector('div');
        btn.addEventListener('click', function() {
            // console.log(location.href);
            location.href = 'http://www.itcast.cn';
        })
        
        var timer = 5;
        setInterval(function() {
            if (timer == 0) {
                location.href = 'http://www.itcast.cn';
            } else {
                div.innerHTML = '您将在' + timer + '秒钟之后跳转到首页';
                timer--;
            }

        }, 1000);
```





## 6.navigator对象

1.navigator 对象包含有关浏览器的信息，他有很多属性，我们最常用的是userAgent，该属性可以返回由客户机发送服务器的user-agent头部的值。

2.利用一下前端代码可以判断用户哪个终端打开了页面，实现跳转。

```
if((navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|
Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|WebOS|
Symbian|Windows Phone)/i))) {
    window.location.href = "";     //手机
 } else {
    window.location.href = "";     //电脑
 }
```



## 7.history对象

window 对象给我们提供了一个history对象，与浏览器历史记录进行交互。该对象包含用户（在浏览器窗口中）访问过的URL。

- back() 可以后退功能
- forward（）前进功能
- go（参数） 前进后退功能。如果参数是1前进，如果是-1后退1个页面。

> index.html

```

<body>
    <a href="list.html">点击我去往列表页</a>
    <button>前进</button>
    <script>
        var btn = document.querySelector('button');
        btn.addEventListener('click', function() {
            // history.forward();
            history.go(1);
        })
    </script>
</body>
```

> list.html

```
<body>
    <a href="index.html">点击我去往首页</a>
    <button>后退</button>
    <script>
        var btn = document.querySelector('button');
        btn.addEventListener('click', function() {
            // history.back();
            history.go(-1);
        })
    </script>
</body>
```



# 第十四章 PC端网页特效

## 1.元素偏移量offset系列

1.使用offset系列相关属性可以动态的得到该元素的位置（偏移）、大小等。

- 获得元素距离带有定位父元素的位置；

- 获取元素自身的大小（宽度高度）。
- 返回的值都不带单位。

```
  // offset 系列
        var father = document.querySelector('.father');
        var son = document.querySelector('.son');
        
        // 1.可以得到元素的偏移 位置 返回的不带单位的数值  
        console.log(father.offsetTop);
        console.log(father.offsetLeft);
        
        // 它以带有定位的父亲为准  如果么有父亲或者父亲没有定位 则以 body 为准
        console.log(son.offsetLeft);
        
        var w = document.querySelector('.w');
        // 2.可以得到元素的大小 宽度和高度 是包含padding + border + width 
        console.log(w.offsetWidth);
        console.log(w.offsetHeight);
        
        // 3. 返回带有定位的父亲 否则返回的是body
        console.log(son.offsetParent); // 返回带有定位的父亲 否则返回的是body
        console.log(son.parentNode); // 返回父亲 是最近一级的父亲 亲爸爸 不管父亲有没有定位
```

2.offset 与 style 区别 

> **offset**
>
> offset 可以得到任意样式表中的样式值
>
> offset 系列获得的数值是没有单位的
>
> offsetWidth 包含padding+border+width
>
> offsetWidth 等属性是只读属性，只能获取不能赋值
>
> 所以，我们想要获取元素大小位置，用offset更合适

> **style**
>
> style 只能得到行内样式表中的样式值
>
> style.width 获得的是带有单位的字符串
>
> style.width 获得不包含padding和border 的值
>
> style.width 是可读写属性，可以获取也可以赋值
>
> 所以，我们想要给元素更改值，则需要用style改变

## 2.元素可视区client系列



![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126162147991.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 

```
        // client 宽度 和我们offsetWidth 最大的区别就是 不包含边框
        var div = document.querySelector('div');
        console.log(div.clientWidth);
```



## 3.元素滚动scroll系列

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126162236634.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126162251752.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019112616230843.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126162931852.png) 



- element.offsetWidth:返回自身包括padding、**边框**、内容区的宽度，返回值不带单位；
- element.clientWidth:返回自身包括padding、内容区的宽度，不含边框，返回数值不带单位；
- element.scrollWidth:返回自身实际的宽度，不含边框，返回数值不带单位。



**扩展**：立即执行函数

1.立即执行函数: 不需要调用，立马能够自己执行的函数

```
        function fn() {
            console.log(1);
        }
        fn();
```

2.写法 也可以传递参数进来(function() {})()    或者  (function(){}());

```
 (function(a, b) {

            console.log(a + b);

            var num = 10;

        })(1, 2); // 第二个小括号可以看做是调用函数

```

```
        (function sum(a, b) {

            console.log(a + b);

            var num = 10; // 局部变量

        }(2, 3));

```

3.立即执行函数最大的作用就是 ：独立创建了一个作用域, 里面所有的变量都是局部变量 不会有命名冲突的情况 



![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126163022333.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 



## 4.动画函数封装

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126163106530.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 

```
  var div = document.querySelector('div');
        var timer = setInterval(function () {
            if (div.offsetLeft >= 400) {
                // 停止动画 本质是停止定时器
                clearInterval(timer);
            }
            div.style.left = div.offsetLeft + 1 + 'px';
        }, 3);
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126163130104.png) 

```
   // 简单动画函数封装obj目标对象 target 目标位置
        function animate(obj, target) {
            var timer = setInterval(function() {
                if (obj.offsetLeft >= target) {
                    // 停止动画 本质是停止定时器
                    clearInterval(timer);
                }
                obj.style.left = obj.offsetLeft + 1 + 'px';

            }, 30);
        }
        
        // 调用函数
        animate(div, 300);
        animate(span, 200);
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126163140922.png) 

```
        function animate(obj, target) {
            // 当我们不断的点击按钮，这个元素的速度会越来越快，因为开启了太多的定时器
            // 解决方案就是 让我们元素只有一个定时器执行
            // 先清除以前的定时器，只保留当前的一个定时器执行
            clearInterval(obj.timer);
            
            obj.timer = setInterval(function() {
                if (obj.offsetLeft >= target) {
                
                    // 停止动画 本质是停止定时器
                    clearInterval(obj.timer);
                }
                obj.style.left = obj.offsetLeft + 1 + 'px';

            }, 30);
        }
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191126163148795.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpZWFubmExMjM=,size_16,color_FFFFFF,t_70) 

```
 function animate(obj, target) {
           
           // 先清除以前的定时器，只保留当前的一个定时器执行
            clearInterval(obj.timer);
           
           obj.timer = setInterval(function() {
                
                // 步长值写到定时器的里面
                var step = (target - obj.offsetLeft) / 10;
               
               if (obj.offsetLeft == target) {
                    // 停止动画 本质是停止定时器
                    clearInterval(obj.timer);
                }
               
               // 把每次加1 这个步长值改为一个慢慢变小的值  步长公式：(目标值 - 现在的位置) / 10
                obj.style.left = obj.offsetLeft + step + 'px';

            }, 15);
        }
```



## 5.常见网页特效案例





# 第十五章 移动端网页特效

## 1.触屏事件

## 2.移动端常见特效

## 3.移动端常用开发插件

## 4.移动端常用开发框架





