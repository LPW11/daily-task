变量/对象（属性和方法）

把什么类型的数据赋值给变量（**这其实就是创建新实例，其实不完全是注意区别**），其实所有的数据类型都是对象因为他们有各自的属性和方法，所以当变量声明之后改变量就有了对应的属性和方法

### 数组(数组是指用一个变量表示一个值的集合,集合中的每个值都是这个数组的一个元素 （element)

- attention：
  - 字符串、数值和布尔值都是标量（scalar）。如果某个变量是标量，它
    在任意时刻就只能有一个值

- 数组的声明：
  - 关键字声明：var 变量名 = Array(数组初始元素个数：长度，也有可能不知到有几个也可以不写)
    - 创造(声明)了数组之后要进行填充：要给出新元素的值还要给出新元素的存放位置  ：array[index] = element
    - 获取元素的方式：数组的变量名[index]
  - 声明数组的同时进行填充（这种方式要求用逗号把各个元素隔，会自动匹配下标）
    - var beatles = Array( "John", "Paul", "George", "Ringo" );
    - var beatles = [ "John", "Paul", "George", "Ringo" ];
    - var 数组名 = [ ] (里面什么都不写创造一个空的数组)

- 存放元素到数组里(element可以的种类)
  - 可以是已经赋值了的变量所代表的数据类型（像数组也是可以的）
  - 可以是另外一个数组里的元素

- 查询数组的方式

  - 数组名[ ]

  

  

### 对象：也是使用一个名字表示一组值。对象的每个值都是对象的一个属性：对象名 {关键字(属性名):值}

- 对象字面量

  - **对象字面量**是一个包含**零对**或**多对属性名称**和**对象关联值**的**列表**，用花括号 ( `{}`)括起来

    - `car`对象的第一个元素定义了一个属性`myCar`，并为其分配了一个新字符串“ `Saturn`”；第二个元素，`getCar`属性，立即分配调用函数的结果`(carTypes("Honda"))`；第三个元素`special`属性使用现有变量 ( `sales`)

    - var sales = 'Toyota';

      function carTypes(name) {
        if (name === 'Honda') {
          return name;
        } else {
          return "Sorry, we don't sell " + name + ".";
        }
      }

      var car = { myCar: 'Saturn', getCar: carTypes('Honda'), special: sales };

      console.log(car.myCar);   // Saturn
      console.log(car.getCar);  // Honda
      console.log(car.special); // Toyota

  - 属性名称的设置

    - 使用**数字**或**字符串文字**作为属性名称或将对象嵌套在另一个对象中。以下示例使用这些选项

    - var car = { manyCars: {a: 'Saab', b: 'Jeep'}, 7: 'Mazda' };

      console.log(car.manyCars.b); // Jeep
      console.log(car[7]); // Mazda

    - 可以是任何字符串，包括空字符串(不是有效标识符的属性名称不能作为点 ( `.`) 属性访问，但*可以*使用类似数组的符号 (" `[]`")访问和设置)

      

  - 有效访问

    - 属性和方法都使用 “点”语法来访问Object.property/Object.method()

    - var unusualPropertyNames = {
        '': 'An empty string',a
        '!': 'Bang!'
      }
      console.log(unusualPropertyNames.'');   // SyntaxError: Unexpected string
      console.log(unusualPropertyNames['']);  // An empty string
      console.log(unusualPropertyNames.!);    // SyntaxError: Unexpected token !
      console.log(unusualPropertyNames['!']); // Bang!

  - 属性

    - 属性是隶属于某个**特定对象的变量**

    - 对象是**自包含的数据集合**，包含在**对象里的数据**可以通过两种形
      式访问——**属性 （property）和方法 （method）**

    - 对象可以被看作是一组属性的集合
    - 用 [对象字面量语法](https://developer.mozilla.org/en-US/JavaScript/Guide/Values,_variables,_and_literals#object_literals) 来定义一个对象时，会自动初始化一组属性
      - 如果你定义了一个对象，var a = {}，那么 a 就会自动有 a.hasOwnProperty 及 a.constructor 等属性和方法
    - 属性使用**键**来标识，它的**键值**可以是一个**字符串或者符号值（Symbol）**

  - 方法:方法是只有**某个特定对象**才能调用的函数

  - ![image-20210818140218433](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210818140218433.png)

  - 给对象创造实例（对象可能代表着某类东西，把某类的东西更细化的时候需要用到实例）

    - var jeremy(新实例) = new(关键字) Person(对象名);
    - 我们就可以
      像下面这样利用Person 对象的属性来检索关于jeremy 的信息了：
    - jeremy.age
      jeremy.mood

    

- 对象的创建：

  - 使用Object 关键字
    - var lennon(对象名) = Object(关键字)();
      lennon.name(属性名/键名) = "John"(键值名);
      lennon.year = 1940;
      lennon.living = false;
  - 花括号语法
    - var lennon = { name:"John", year:1940, living:false };

- 对象和数组最大的不同

  - 对象来代替传统数组的做法意味着**可以通过元素的名字**而不是下标数
    字来引用它们。

    - var beatles = Array();
      beatles[0] = lennon;

      beatles = [{ name:"John", year:1940, living:false }]

    - 若想访问则要——使用 beatles[0].name 得到值“John”而不是beatles[0][0]

    - var beatles = {};
      beatles.vocalist = lennon;

      Beatles = {vocalist = {name:"John", year:1940, living:false}}

      现在，beatles.vocalist.name 的值
      是“John”，beatles.vocalist.year 的值是
      1940，beatles.vocalist.living 的值是false.

      

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    