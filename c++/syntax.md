C++ 是一种静态类型的、编译式的、通用的、大小写敏感的、不规则的编程语言，支持过程化编程、面向对象编程和泛型编程。

***

面向对象编程：

- 封装

  数据和方法组合在一起；

- 继承

  从已有的类中派生出新类，新类具有已有的类的属性和方法；

  ```python
  from torch import nn
  class LayerNorm(nn.module):
  	super.__init__()
  ```

- 多态

  指同一种操作作用不同的对象，可以有不同的解释和实现

- 抽象

  抽象类和接口

***

标准库

- 核心语言
- C++标准库
- 标准模板库（STL)

***

ANSI标准

保证C++的便携性

***

基本语法

1. 对象
2. 类
3. 方法
4. 即时变量:每个对象独特的即时变量

```c++
#include <iostream>
//头文件，c++标注库的接口说明书
using namespace std;
//告诉编译器使用std命名空间，命名空间就是作用域
//main是程序开始的地方
int main()
{
    cout<<"Hello,World!"<<endl;
    return 0;
}
```

`;`分号是语句结束符

语句块是一组使用大括号，括起来的逻辑连接语句

c++不以行为结束符标志

***

c++标识符

字母 A-Z 或 a-z 或下划线 _ 开始，后跟零个或多个字母、下划线和数字（0-9）

***

**c++内置类型**

bool布尔型

char字符型

int整型

float浮点型

double双浮点型

void无类型

wchar_t宽字符型

auto自动判断



decltype获取表达式的类型

nullptr空指针常量

std::initializer_list初始化列表类型

std::tuple元组类型

**修饰符**

signed

unsigned

short

long

const

volatile

mutable

**派生数据类型**

数组

指针

引用

函数

结构体

类

联合类

枚举

**类型别名**

typedef

using

**标准库类型**

std::string

std::vector

std::array

std::pair

std::map

std::set

**类型转化**

1. 静态转化

```c++
int i=10;
float f = static_cast<float>(i)
```

2. 动态转化

```python
dynamic_cast<目标类型>(表达式)
```

3. 常量转化

4. 重新解释转化

***

c++类的定义方法

```c++
class classname//关键字 类名
{
    Access specifiers://访问修饰符：private/public/protected
    	Date members/variables;
    	Member functions(){}//成员
}
```

这个里面说明函数说明，并不是抽象函数

```c++
class abram{
    public:
    	double age;
    	double get(void);//成员函数声明
}
double abram::get(void)
//double 返回类型，abram类：：作用域
{
    return age;
}    
```

`::` 作用域解释运算符

`<<`流插入运算符

```c++
#include<iostream>
using namespace std;
int main{
    cout<<"hello,world"<<endl;
    return 0;
}
```

这里的`cout`，`endl`是std命名空间

这个`namespace`指得是定义的范围是怎么样的，这个是提前定义好的

***

