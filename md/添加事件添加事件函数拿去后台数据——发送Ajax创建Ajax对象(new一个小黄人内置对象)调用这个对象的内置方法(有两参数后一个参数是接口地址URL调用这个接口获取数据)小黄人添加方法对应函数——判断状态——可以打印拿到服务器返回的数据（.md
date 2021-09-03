- ![image-20210902094008742](C:\Users\wenyi.lu\AppData\Roaming\Typora\typora-user-images\image-20210902094008742.png)

- 添加事件

- 添加事件函数

- 拿去后台数据——发送Ajax
  - 创建Ajax对象(new一个小黄人内置对象)
  
  - 调用这个对象的内置方法(有两参数后一个参数是接口地址URL调用这个接口获取数据)
  
  - 小黄人添加方法对应函数——判断状态——可以打印拿到服务器返回的数据（在控制台中可以看到）——拿到数据如何渲染到服务器页面上呢？——数据的格式可能是`json`字符串格式所以我们要把它转成`js`对象
  
  - `xhr.onreadystatechange = function() {`
  
    ​	`if(xhr.readyState ==4 && xhr,status == 200){`
  
    `		console.log(xhr.responseText);`
  
    ​	`var data = xhr.responseText;`
  
    `data = JSON.prase(data)`
  
    ``}}```
  
  - 发送方法

