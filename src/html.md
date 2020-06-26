# HTML 规范

- Html5 doctype 

  - 页面的doctype使用标准的模式

  - 例：

    ```html
    <!DOCTYPE html>
    <html lang="en">
      ...
    </html>
    ```

- 字符编码

  - 使用UTF-8

  - 例：

    ```html
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8"/>
      </head>
      <body>
        ...
      </body>
    </html>
    ```

- 属性

  - 属性全部小写
  - 使用双引号
  - 书写顺序
    - class -- 组件复用设计
    - id -- 不建议使用
    - name
    - src，for，type，href，value，maxLength，max，min，pattern
    - placeholder，title，alt
    - required，readonly，disabled

- 兼容模式

  - 使用meta指定IE渲染版本

  - 例：

    ```html
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="IE=Edge">
      </head>
      <body>
        ...
      </body>
    </html>
    ```

- 其他

  - 引入css、js时不需要指明type
  - 编写html时，避免使用多余的父节点
  - 书写结构型的标签时使用html5的结构标签，如：nav，section等
  - 缩进等按照lint规范