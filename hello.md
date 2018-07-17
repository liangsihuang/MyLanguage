# 模块化

### Python : module

一个`. py` 文件就是一个模块 module

模块的多级目录：包 package，用处：可以重复命名

* 文件夹： MyPackage

* 识别为包的必要文件：`双下划线`_init_`双下划线` .py

* 模块：classLib.py

类库：

* 普通目录      `from classLib(filename) import Equation(classname)`

* 包         `from MyPackage.classLib(filename) import Equation(classname)`

模块搜索路径：

* sys.path
* 一般是：当前目录
* 添加     sys.path.append\( '.../my\_py' \)

### C++ : h file

类的接口： h 文件

* 内联函数可以在 h 文件实现

类的方法实现： cpp 文件

导入 \#include &lt;mmm.h&gt;

* 编译器中的类库路径

导入 \#include "mmm.h"

* 当前目录



