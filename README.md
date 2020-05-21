

# 一、简答题

1. `10`		原因： i 属于全局作用域，循环结束的时候值为10，数组中存储的函数调用的i都为10

2. 报错 ReferenceError，let 定义变量 tmp，变量声明会被提升，但是没有初始化，调用会报错

3. ```javascript
   const min = Math.min(...arr)
   ```

4. 1. var 声明的变量都在全局变量中，let 和 const 声明的变量不会
   2. var 声明的变量存在变量提升，let 和 const 不存在变量提升
   3. let 和 const 声明会形成块作用域
   4. const 为常量，为基本类型时不能改变，为对象时不能修改引用地址

5. `20`      原因：obj.fn() 方法执行的时候 this 指向 obj对象，setTimeout 中使用箭头函数，this的指向obj对象

6. 用途:

   1. 阻止对象属性名冲突 
   2. 模拟私有属性

7. - 浅拷贝: 复制一层对象的属性，遇到引用类型会复制引用地址，修改引用类型的数据会影响原对象
   - 深拷贝: 复制对象以及对象的所有子对象，修改后不会影响原对象

8. EventLoop是js的事件循环机制，同步任务会进入主线程，异步任务分为微任务和宏任务，微任务执行完，会执行宏任务，然后重复整个过程。

   宏任务： IO、setTimeout、setInterval

   微任务： Promise.then、process.nextTick

9. ```javascript
   var promise = Promise.resolve('hello')
   promise.then(res => res + 'lagou').then(res => console.log(res + 'I ❤️ U'))
   ```

10. TypeScript 是 JavaScript 的超集，即包含 JavaScript 的所有元素，能运行JavaScript 的代码，并扩展了JavaScript 的语法。相较于 JavaScript，还增加了静态类型、类型注解、类、接口、泛型等方面的功能，更易于大项目的开发。

11. - 优点: 增加了代码的可读性和可维护性、非常包容，可以直接使用js代码
    - 缺点: 增加了很多新概念（接口、泛型、枚举等），增加了一定的学习成本、短期项目可能会增加一些开发成本