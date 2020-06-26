# Vue组件

优先遵循项目组件的声明规则进行开发

- 组件原则

  - 公用组件和元组件设计遵循基础项目的规则进行编写
  - 功能设计和业务耦合保持最低耦合原则
  - props设计尽可能扁平化
  - 辅助代码进行分离
  - 状态管理和State尽可能集中处理

- 组件命名

  - 按照项目组件命名规则执行
  - 必须写name属性

- 组件属性

  - 建议按照官网单向数据流，并且声明传值类型
  - Prop大小写按照项目设置
  - 动态组件和异步组件代替 v-if切换渲染组件

- 组件html

  - 自定义组件 使用单一标签

    ```html
    <my-component />
    ```

  - 组件属性书写顺序

    - 指令
    - 属性
    - 事件

    ```html
    <my-component
      v-if="condition"
      v-show="condition"   
      v-model="value"
      :selfDefined="myAttr"
      :placeholder="i18n.holder"
      @click="clickHandle"
      @hover="hoverHandle"
    />
    ```

- 组件style

  - 使用 scoped 
  - 使用less
  - 需要覆盖 ui 框架的样式 /deep/
  - 需要全局覆盖的样式在根组件下引入

- 组件等级

  - 业务组件区分与基础元组件
  - 基础元组件放置在src下的component
  - 业务组件在相关目录下建component放置

- ​	其他

  - 运行时，需要频繁切换的组件使用 v-show，很少改变时使用v-if
  - v-for时一定要加上key
  - Props加入类型声明和必传
  - 属性换行书写
  - html template 的渲染条件复杂时，请使用method或者computed做过滤
  - 组件尽量使用动态组件进行懒加载