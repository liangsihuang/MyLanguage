# data structure

## C++  array

指针数组，也可以用 `[]` 索引

```cpp
int *arr = new int[10];

for(int i=0; i<10; i++)
    arr[i] = i

delete[] arr;
```

## C++ container

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

## Map

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

## python 字典 dict

key 必须是不可变的数据类型：int, string

调用：

* d = {}
* d = { key : value }
* d\[key\] = value

快速返回值：d\[key\]

* 如果没找到，会调用自定义的missing方法
* ```python
  def __missing__(self, key):
      return 0
  ```
* 如果不定义，没找到就会报错！

更安全地返回指定key的值：d.get\(key, defalut=0\) ，没找到返回0，如果不给defalut，默认default为None

key存在否：d.\_\_contains\_\_\(key\)，存在返回 true，否则返回false

遍历：items\(\)方法

```py
for k, v in dictName.items():
    print(k, v)

# or 
for k in dictName:
    print(dictName[k])
```

元素个数：len\(\)

删除元素：pop\(key\)，返回对应的 value

## python 列表 list

range\(start, end, step\) 返回一个列表

* 左闭右开
* step 默认为1
* 常用： `for i in range(1,10)` 1到9

len\(\)：返回个数，有5个元素，下标到4，但返回5

append\(\)：在末尾添加

## numpy 矩阵类ndarray

类的名字是ndarray，其中有一个方法叫array（代替构造函数）

```python
import numpy as np
a = np.array([1，2，3])
```

参数是一个列表

* 向量：a = array\(\[1, 2, 3\]\)
* 矩阵：b = array\(\[ \[1, 2, 3\], \[3, 2, 1\] \]\)

限定数据类型：a = np.array\(\[1,2\], np.int\)

全0列向量阵：a = np.zeros\( \(2, 1\), dtype=int \)

所有元素个数： np.size\(a\)

* 一行元素的个数：np.size\(a, 0\)
* 一列元素的个数：np.size\(a, 1\)

可以切片：左闭右开。 全选：x\[:\]

