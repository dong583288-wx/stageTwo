## JavaScript 介绍

  > JavaScript是什么?

    JavaScript是一种专为网页交互而设计的脚本语言.

  > JavaScript的起源

    时间：1995年

    人物：Brendan Eich（布兰登·艾奇）

    背景：那个时候，绝大多数因特网用户都是用速度仅为28.8kbit/s的「猫」上网，为了完成简单的表单验证，必须把表单数据发送到服务器端才能确定用户是否没有填写某个必填域、是否输入了无效的值，每次操作需等待30秒以上才会有结果，这无疑是在慢性自杀。

    事件：当时走在技术革新最前沿的 Netscape 公司指派Brendan Eich 开发一种客户端语言，用来处理这种简单的验证，它就是JavaScript。JavaScript 原名 LiveScript，Netscape 为了搭上媒体热炒 Java 的顺风车，才把LiveScript 改名为 JavaScript。（所以 Java 和 JavaScript 的关系，就相当于菠萝和菠萝蜜的关系。）

    自此以后，JavaScript 逐渐成为市面上常见浏览器必备的一项特色功能。如今，JavaScript 的用途早已不再局限于简单的数据验证，而是具备了与浏览器窗口及其内容等几乎所有方面交互的能力。今天的 JavaScript 已经成为一门功能全面的编程语言。


  > JavaScrpit的应用场景

    1. 网页交互
    2. 服务端开发(Node.js)
    3. 命令行工具(Node.js)
    4. 桌面程序(Electron)
    5. App(Cordova)
    6. 控制硬件-物联网(Ruff)
    7. 游戏开发(cocos2d-js)

  > JavaScript的组成

    ECMAScript-JavaScript的核心

      定义了JavaScript的语法规范描述了语言的基本语法和数据类型，ECMAScript是一套标准，定义了一种语言的标准与具体实现无关

    BOM-浏览器对象模型

      一套操作浏览器功能的API 通过BOM可以操作浏览器窗口，比如：弹出框、控制浏览器跳转、获取分辨率等

    DOM-文档对象模型

      一套操作页面元素的API   DOM可以把HTML看做是文档树，通过DOM提供的API可以对树上的节点进行操作
  > \<script>元素

    向HTML页面中插入JavaScript的主要方法,就是使用<script>元素,这个元素是由Netscape创造并首先实现的.

    方法一: 直接在\<script>元素中写JavaScript

      <script>
        // 在这里写代码
      </script>

    方法二: 新建一个单独的js文件,比如 example.js 通过scr引入外部资源文件

      <script src="example.js"></script>

  > 注释

    单行注释

      // 注释内容

    多行注释

      /*
       * 注释内容
       *
       */
  

## JavaScript 语法
  > 变量

    当程序需要将值保存起来以备将来使用时，便将其赋值给一个变量，值的类型称作数据类型。

  + 声明一个变量:

    var 变量名;

  + 声明多个变量:

    var 变量名,变量名,变量名;

  + 声明一个变量并赋值:

    var 变量名 = 值;

  + 声明多个变量名并赋值:

    var 变量名 = 值,变量名 = 值,变量名 = 值; 

  + 变量的命名规则(必须遵守,不遵守会报错):

      区分大小写
      由字母、数字、下划线、$符号组成，不能以数字开头
      不能是关键字和保留字，例如：for、while。
    
  + 变量的命名规范(最好遵守):

      变量名必须有意义
      遵守驼峰命名法。首字母小写，后面单词的首字母需要大写。例如：userName、userPassword

  > 数据类型

    简单数据类型:
    String类型--字符串  Number类型 --数字  Boolean类型--布尔  Undefined类型--未定义 Null-空对象指针

    复杂数据类型:
    Object--对象

  > 数据类型检测(typeof 操作符)

      格式:  typeof 值
      结果:
            "string" -- 如果这个值是字符串
            "number" -- 如果这个值是数字
            "boolean" -- 如果这个值是布尔值
            "undefined" -- 如果这个值未定义
            "objet" -- 如果这个值是对象或null
            "function" -- 如果这个值是函数 
  > String数据类型

    String数据类型,其实就是字符串,它表示由零个或多个字符组成的字符序列.

  + 格式: 字符串是由一对双引号(")或单引号(')引起来的字符序列

    var sName = "wanlum";
    var sHobby = 'reading';

  + 特点

    JavaScript中声明的字符串是不可变的.要改变某个变量保存的值,必须销毁前一个值,才能把新的字符串赋值给变量

  + 检测

    var sMessage = 'Hello,World';
    console.log(typeof sMessage); // "string" 

  + 转换

    把一个值转换为一个字符串有两种方式:

    方式一: 使用toString()方法,适用于数值 布尔值 字符串 对象

      var intAge = 18; //数字

      var bFlag = true; // 布尔值

      var sName = 'wanlum'; // 字符串

      console.log(intAge.toString());

      console.log(bFlag.toString());

      console.log(sName.toString());
      
    方法二: 使用String()方法,适用于不知道值的数据类型的情况下

      var intAge = 18; //数字

      var bFlag = true; // 布尔值

      var sName = 'wanlum'; // 字符串

      var sMessage = undefined; // 未定义

      var oCar = null; // 空对象指针

      console.log(String(intAge));

      console.log(String(bFlag));

      console.log(String(sName));

      console.log(String(sMessage));

      console.log(String(oCar));

  > Number数据类型

    Number数据类型,其实就是数字.它表示值得大小,多少等等

  + 格式: 

    var intAge = 18;
    var floatHeight = 1.74;

  + 检测

    var intAge = 18;
    console.log(typeof intAge); // "number" 

  + 按精度分类

    整型: 就是整数 

      var intAge = 20;

    浮点型: 就是小数

      var floatWeight = 45.4;

  + 按进制分类

    十进制: 由0-9这十个数字组成

      var decNumber = 9;

    二进制: 由0-1这两个数字组成

      var binNumber = 101010100101;
    
    八进制: 由0-7这八个数字组成且第一位必须是0;

     var oct = 077;

    十六进制: 由0-9及A-F且必须以0x开头  A-F可大写也可小写
  
  + 取值范围

    最大值: Number.MAX_VALUE 值为:1.7976931348623157e+308

    最小值: Number.MIN_VALUE 值为:5e-324

    无穷大: Infinity
    无穷小: -Infinity
  
  + 特殊数字--NaN

    NaN: 英文: not  a number 意思是: 不是一个数字
    NaN与任何值都不相当,包括它本身
  + 数据类型转换

    把一个值转换为数字类型总共由三种方式:

    方式一: 使用Number()方法  该方法适用于任何类型的数据

    方式二: 使用parsetInt()方法 该方法适用于字符串

    方法三: 使用parseFloat()方法 该方法适用于字符串
  > Boolean数据类型

    Boolean数据类型,其实就是判断真或假也就是true或false,Boolean数据类型只有这两个值.

  + 格式

    var bMarried = false;
    var bFlag = true;

  + 检测

    var bMarried = false;

    console.log(typeof bMarried); // "boolean" 
  
  + 取值范围

    Boolean数据类型只有两个值: 
      如果判断为真,则为true
      如果判断为假,则为false

  + 转换
  
    把一个变量转换为布尔类型变量共有一种方式:

    方式一: Boolean()

      转换为true的数据有: 任何非空字符串,任何非零数值(包括无穷大) 任何对象  

      转换为false的数据有: 空字符串,零和NaN,null,undefined

  > Undefined数据类型
    Undefined数据类型,就是特殊的undefined.在使用var声明变量但并没有给变量值的时候,就会有一个默认值undefined

  + 格式

    var sName;

    console.log(sName == undefined); // true

  + 检测

    console.log(typeof undefined); // undefined

  + 取值范围

    只有一个值: undefined

  + 最佳实践

    无论什么情况下,都没有必要把一个变量的值显式设置为undefined
  
  > Null数据类型

    Null数据类型是第二个只有一个值的数据类型,它的值是null.  null值表示一个空对象指针,也就是一个空对象.

  + 格式

    var car = null;
  
  + 检测

    console.log(typeof car); // object

  + 取值范围

    只有一个值: null

  + 最佳实践

    如果一个变量准备在将来用于保存对象,最好将该变量初始化为null
## javaScript 操作符

  > 一元运算符

  > 布尔运算符

  > 关系运算符

  > 赋值运算符

  > 运算符的优先级