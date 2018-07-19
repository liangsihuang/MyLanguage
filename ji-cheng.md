为什么类的初始化，两边类型不同？public 继承的赋值兼容规则

`LinearSOE * theSOE = new BandSPDLinSOE( * theSolver);`



### C++

默认是 public 继承 `class DeriveClassName : public BaseClassName {}`

* 派生类的对象可以赋值给基类对象！实现多态的一个关键！

* 派生类对象可以初始化基类引用

* 派生类对象的地址可以赋值给基类指针

派生类拥有基类的所有成员变量和函数（无论 private, protected, public）

* 但是派生类的成员函数，不能访问基类的 private 成员
* 可以访问基类的 protected 成员

成员函数可以覆盖，覆盖以后还可以调用基类的同名函数

* `BaseClassName:: Func`

### 多继承

C++ 和 python 都支持

