# constructor

一般的初始化方式：在构造函数体内进行赋值操作

c++ 的统一初始化方式：初始化列表

* 能够初始化一般成员变量：int, double
* 能够初始化类成员变量：Vector, 自定义类
* 能够初始化父类（即父类继承来的变量）

## 析构函数 destructor

C++ 一般要自己写，因为要释放 new 出来的空间

```cpp
~ className(){}
```

python 有垃圾回收机制，一般不必写

```python
def __del__(self):
    pass
```

c++和python都是出了作用域后自动调用。python 可以强制调用

```python
del objectName
```

