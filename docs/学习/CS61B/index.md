# CS61B


## 数据

### 1. SLLists, Nested Classes, Sentinel Nodes
  - 运用递归方法得出基础nodelist，再用SLList封装（private static nodelist）,得到更好调用和安全的链表，然后再用加一个中间节点[Sentinel Nodes](https://github.com/Berkeley-CS61B/lectureCode-fa20/blob/master/lists2/SLList.java),在不添加特殊情况下防止节点开头是null造成的错误，保持一致性，进一步可以在尾部加多一个Sentinel Node，可以反向遍历
  - private修饰类表示只在该类所在（上层）类内访问（外对内），static修饰表示该类无需访问外部（内对外）
  - 在嵌套的时候不要忘记实例化

### 2.Interface Inheritance（implement）和Implementation Inheritance（extend）
  - 前者更多是起到提示和检测，以及方便调用，只声明方法和默认方法（default），在调用是更像是一个放大的泛型，都提供了抽象/约束，增加复用性和灵活性
  - 后者是复用全部，但是可能会出现无法访问父类的private类，此时用super
  - 两者都可以用@override，这更多是一个提醒有无拼写错误和这个方法复写

### 3.Extends, Casting, Higher Order Function
  - casting类型转换，就是父子类互相转换（其中子类转父类要显性 Dog dog = (Dog) animal），目的一般来说服务于多态或者联通外部
  - java的高阶函数使用方法（.apply）本质上是接口继承

### 4.comparator
   - java内置的比较器类，方便排序查找，也可自定义


## 设计

### 1. Pipeline（分步）和State Pattern（状态）
  - 如果是线性的，流程固定的，选择前者为主（2048先合并再移动）
  - 如果是多种可能的状态转换，用后者（游戏角色的举动）



## 算法
