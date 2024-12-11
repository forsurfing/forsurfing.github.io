# CS61B


## 数据

### 1. SLLists, Nested Classes, Sentinel Nodes
  - 运用递归方法得出基础nodelist，再用SLList封装（private static nodelist）,得到更好调用和安全的链表
  - private修饰类表示只在该类所在（上层）类内访问（外对内），static修饰表示该类



## 算法

### 1. Pipeline（分步）和State Pattern（状态）
  - 如果是线性的，流程固定的，选择前者为主（2048先合并再移动）
  - 如果是多种可能的状态转换，用后者（游戏角色的举动）