# Css&Less

- 命名

  - 类名及id全部小写，中划线分隔

  - 例：

    ```css
    .my-class {
      font-size: 20px;
    }
    #my-id {
      background: transparent;
    }
    ```

    

- less变量

  - 变量、函数、混合等采用驼峰式命名

    ```less
    @baseColor: #f938ab;
    @successColor: green;
    @warnColor: red;
    .box {
      background: @baseColor;
    }
    ```

  - 更多 [Less]()

- 注释

  - css注释 统一使用 “ /* .... */ ” ，Less中相同

  - 例： 

    ```css
    /* 模块导航 */
    .module-header {}
    /*
     * 模块导航
     * @xiewenqiang-Jason
     */
    .module-header {}
    ```

- ​	属性合并

  - 相关属性的声明尽量做分组处理，组之间使用空行

  - 例：

    ```css
    .my-box {
      display: flex;
      just-content: space-bewteen;
      
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 1;
      
      font: normal 13px "Helvetica Neue", sans-serif;
      line-height: 1.5;
      text-align: center;
      
      border: 1px solid #e5e5e5;
      border-radius: 3px;
      width: 100px;
      height: 100px;
    }
    ```

- 分号与引号

  - 必须书写分号
  - 使用双引号

- 组件css

  - 参照Vue组件style规范

- 其他
  - 颜色：使用小写字母，能简写就简写
  - 媒体查询或者相关规则，尽量将规则放置在最近位置，不要将其放置到独立文件或者文件的底部
  - 去掉小数点前面的0
  - 属性为0的不要加单位
  - 相同规则复用 （less）
  - 不要使用 * 选择器
  - 不用的类或者规则，删除
  - 不需要前缀书写-编译器自动添加