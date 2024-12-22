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

### 5.Binary search tree
   - 通过简单的二分类，将数据分割排序，查找时间复杂度$O（\log n）$
   - 一个父节点只能有两个子节点，一个节点内只能有一个数据
  
### 6.B-tree
  - 类似二叉树，但是一个父节点可以有四个子节点，同时一个节点也可以有三个数据
  - 这降低了树的高度，同时更加平衡
  - 但客观来说，我还不知道为什么这样能带来好处

### 7.red black tree
  - 存在一一对应的B-tree
  - 通过旋转达到变换 

### 8.hash table
  - 类似查找表（通过hashing函数分类），但是表头不是固定的，而是随着总量增大而增多，每个表头用链表相连【链式地址法（拉链法）】
  - 以此保证整体查找和插入时间低
  - 本质上就是一种n进制重排

### 9.heap
  - 类似树，但是从大到小向下排，可存在相同
  - 处理最优队列问题

## 设计

### 1. Pipeline（分步）和State Pattern（状态）
  - 如果是线性的，流程固定的，选择前者为主（2048先合并再移动）
  - 如果是多种可能的状态转换，用后者（游戏角色的举动）



## 算法


### 1.归并排序
 - 将两个数组按中位数分割，将大的排序任务变为两个
