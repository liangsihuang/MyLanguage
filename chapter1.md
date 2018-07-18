# Data Structure

### C++ container

常用自定义的容器类： Vector , Map

类的定义才用 模板 template

```cpp
template <typename ElemType>
class Vector {
    public:
        Vector();
        ~Vector();

        ElemType getAt(int index);
        ...
}
```

调用时声明模板对应的类型：`Vector<int> list`

只能存放和声明的同一类型的数据，否则报错 （称为 type-safe）

### Map

map 里的每个元素是 pair 类

* pair类有两个成员变量 first , second
* first 代表 key
* second 代表 value

key - value 都采用 template，调用时都需要声明

调用： Map&lt;int, ClassName&gt; theMap;

* key 的类型是 int , value 的类型是 某个 class

方法：

* 某个元素：theMap\[ 'key' \]

遍历采用迭代器 iterator

* 迭代器是 container 类中定义的类 \(称为：nested class/type\)
* 可以看作一个有方法的指针？

* 调用：`Map<int, ClassName> :: iterator it = theMap.iterator();`

* it 的类型是 Map&lt;int, ClassName&gt;:: iterator



