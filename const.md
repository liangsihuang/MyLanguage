# const

为每一个类添加一个 classTag 有什么用？ classTag 是常量

比如：对于 Node 类

```cpp
#define NOD_TAG_Node 1
```

## define

定义真正的常量\(而不是常变量\)，在预处理\(编译前\)过程中进行替换

在头文件\(classTag.h\)中定义，开头和结尾加预处理指令

```cpp
#ifndef classTags_h
#define classTags_h

#define intType 1
...

#endif
```

实际是定义宏，所以不需要在别的文件 include ， 对吗？

## const: c++关键字

常变量（作为新的变量类型）

* 不能修改的变量： `const int NUMBER = 4;`

常引用

* 不能修改的引用
* 作为函数参数，传入后不能修改（为了传递的效率，不用复制）
* 作为函数返回值不能修改（类似：python 返回值为 tuple，不能修改）

常对象

* 对象初始化后不能修改  `const ClassName objectName`

常量成员函数

* `void getValue() const;`
* 不能修改其作用的对象，主要是不能修改成员变量
* 非常量成员函数也不能调用（因为可能修改成员变量）
* 静态成员变量和静态成员函数都可以用，因为不属于对象

