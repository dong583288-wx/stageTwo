## JavaScript 流程控制语句

  > 表达式

    一个表达式可以产生一个值，有可能是运算、函数调用、有可能是字面量。表达式可以放在任何需要值的地方。

  > 语句

    语语句可以理解为一个行为，循环语句和判断语句就是典型的语句。一个程序有很多个语句组成，一般情况下;分割一个一个的语句

  > 顺序结构

    从上到下执行的代码就是顺序结构,因为程序默认就是由上到下顺序执行的

  > 分支结构(条件语句)

    根据不同的情况,执行对应代码,比如: 如果到中午12点我就吃饭,如果到中午1点我就睡觉

  + if

    ```javascript

      if(条件表达式){
        // 执行语句
      }
    ```
  
  + if...else
    ```javascript
      if(条件表达式) { 
        // 执行语句
      } else {
        // 执行语句
      }
    ```
  + 三元运算符
    ```javascript
      表达式1 ? 表达式2 : 表达式3 
    ```
  + if...else if...else
    ```javascript
      if(条件表达式) {
        // 执行语句
      } else if (条件表达式) {
        // 执行语句
      } else if (条件表达式) {
        // 执行语句
      }
    ```
  + switch语句

    ```javascript
    switch (expression) {
      case 常量1:
        语句;
        break;
      case 常量2:
        语句;
        break;
      case 常量3:
        语句;
        break;
      case 常量n:
        语句;
        break;
      default:
        语句;
        break;
    }
    ```
  > 循环结构
  + while语句

    ```javascript
      // 
      while(循环条件) {
        // 循环体
      }

    ```

  + do...while语句

    ```javascript

      do {
        // 循环体;
      } while (循环条件);
    ```

  + for语句
    ```javascript

      for(初始化表达式1; 判断表达式2; 自增表达式3) {
        // 循环体
      }

    ```
  + continue: 立即跳出当前循环，继续下一次循环（跳到i++的地方）
  + break: 立即跳出整个循环，即循环结束，开始执行循环后面的内容（直接跳到大括号）

