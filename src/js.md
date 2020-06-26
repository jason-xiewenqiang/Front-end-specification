# Javascript

- 缩进，分号，空行，换行 --- 按照ESlint规范

- 注释

  - 单航注释

    - 双斜杠后必须要空格
    - 缩进与下一行代码保存一致

  - 多行注释

    - 至少三行 书写内容一行必须要有个空格
    - 使用原则
      1. 难以理解的代码段
      2. 特殊的hack代码-浏览器相关
      3. 业务逻辑相关代码
      4. 可能出现错误的代码
      5. 关键条件逻辑相关业务

    ```javascript
    if (condition) {
      // if you made it here, then all security checks passed
      allowed();
    }
    
    let jsso = 'Jason'; // one space
    
    /*
     * @Description what do you want
     * @Bababa ...
     */
    function doSomething () {}
    
    ```

    

- 文档注释

  - 各类标签@param，@method
  - 参考 [usejsdoc](https://jsdoc.app/) & [JSDoc Guide](http://yuri4ever.github.io/jsdoc/)
  - 使用文档注释的情况
    - 所有的常量
    - 所有的函数
    - 所有的类

- 变量命名

  - 使用驼峰式命名 （对象属性例外：server返回数据）

  - ID 在变量中使用全大写

  - URL 在变量中使用全大写

  - 常量全大写，使用下划线连接

  - 构造函数 首字母大写

  - jquery对象使用$开头命名

  - 例：

    ```javascript
    let nameMyName = 'Jason';
    const resourceID = '123456';
    const itemURL = '/api/item';
    const MAX_LENGTH = 10;
    
    function Person(name) {
      this.name = name;
    }
    
    var $body = $('body')
    ```

- 变量声明

  - 函数作用域中的变量声明尽量提升至函数首部

  - 未使用的变量，删除

  - 变量要先声明再使用

  - 使用未声明的变量时，检查是否已经在.jslintrc文件中

    ```javascript
    function doSomething (items) {
      // use one var 
      var value = 10,
          result = value + 10,
          i,
          len;
      for (i = 0, len = items.length; i < len; i++) {
        result += 10;
      }
    }
    ```

- 函数

  - 函数声明或者函数表达式的空格遵循lint规则
  - 函数调用括号前不需要空格
  - 参数之间使用逗号分隔，逗号后留空格

- 数组、对象

  - 对象属性名不需要加引号
  - 对象以缩进的形式书写，换行书写
  - 数组、对象最后不留逗号
  - 数组不要出现空元素

- 其他

  - 使用 全等  ‘===’  ‘!==’ 代替 ‘==’  ‘!==’
  - 尽量不要在内置对象上的原型添加方法
  - 不要在比较的地方做赋值
  - 不要在循环内声明函数
  - 尽量使用空格代替tab，不要混用 tab和space
  - 不允许出现空的代码块
  - 对上下文this的引用只能使用_this、that、self其中一个代替

