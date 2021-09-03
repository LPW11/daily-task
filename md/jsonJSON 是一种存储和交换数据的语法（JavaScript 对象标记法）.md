#### json:**JSON 是一种存储和交换数据的语法**（JavaScript 对象标记法）

- What
- why

- 可以做什么
  - 交换数据
  - 发送数据
  - 接受数据
  - 储存数据

- 语法

  - 名称/值由字段名称构成，后跟冒号和值：**名称需要双引号**,**键必须是字符串**

  - 在 JavaScript 中，键可以是字符串、数字或标识符名称：

  - ```javascript
    "name":"Bill Gates"
    ```

  - 在 JSON 中，字符串值必须由双引号编写：

  - ```javascript
    { "name":"Bill Gates" }
    ```

  - 

- JSON和XML均可用于**Web服务器**接受数据

  - 下面的 JSON 和 XML 实例都定义了**雇员对象**，包含了由 **3 个雇员**构成的**数组**

  - ```javascript
    {"employees":[
        { "firstName":"Bill", "lastName":"Gates" },
        { "firstName":"Steve", "lastName":"Jobs" },
        { "firstName":"Elon", "lastName":"Musk" }
    ]}
    ```

- 有效的数据类型

  - 值的数据类型有规定

    - 字符串

    - ```javascript
      { "name":"John" }
      ```

    - 数字

    - ```javascript
      { "age":30 }
      ```

    - 对象（JSON 对象）

    - ```javascript
      {
      "employee":{ "name":"Bill Gates", "age":62, "city":"Seattle" }
      }
      ```

    - 数组

    - ```javascript
      {
      "employees":[ "Bill", "Steve", "David" ]
      }
      ```

    - 布尔

    - ```javascript
      { "sale":true }
      ```

    - null

  - 在 JavaScript 中，以上所列均可为值，外加其他有效的 JavaScript 表达式

    - 函数
    - 日期
    - undefined

- 因为JSON的常规用途是同**Web服务器**进行**数据传输**，在从 **web 服务器接收数据**时，**数据**永远是**字符串**，通过 **JSON.parse() 解析数据**，这些**数据会成为 JavaScript 对象**

  - ![image-20210826155042111](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210826155042111.png)

  - ![image-20210826155820274](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210826155820274.png)

  - ![image-20210826160511756](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210826160511756.png)??????????

  - 所有现代浏览器都有一个**内置的 XMLHttpRequest 对象**来从服务器请求数据。

  - ![image-20210826161035505](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210826161035505.png)
  - 

- 我的疑问
  - 在XMLHttpRequest()方法后想open的地址是以
  - json文件是怎么引入的？