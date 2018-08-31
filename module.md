# module

## Python : module

一个`. py` 文件就是一个模块 module

模块的多级目录：包 package，用处：可以重复命名

* 文件夹： MyPackage
* 识别为包的必要文件：`双下划线`_init_`双下划线` .py
* 模块：classLib.py

类库：

* 普通目录 `from 当前目录某文件夹.classLib(filename) import Equation(classname)`
* 包 `from MyPackage.classLib(filename) import Equation(classname)`

模块搜索路径：

* sys.path
* 包括：当前目录
* 添加     sys.path.append\( '.../my\_py' \)

## C++ : h file + library

类的接口： h 文件

* 函数的参数表：要表明类型，参数名字不重要（可以省略，可以和实现时的参数名字不同）
* 内联函数可以在 h 文件实现

类的方法实现： cpp 文件

* cpp 文件被编译后成为 library \( .lib 文件\)

导入头文件

* \#include &lt;mmm.h&gt; 优先编译器中的类库路径
* \#include "mmm.h" 优先当前目录

在自定义类的头文件不需要include，只需要声明；如果是STL里的类，比如map，声明都不用

* 比如： Class Element; 

在自定义类的cpp文件需要 include

* 比如： \#include &lt;Vector.h&gt;

