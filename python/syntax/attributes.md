```python
__all__ = [list]
# 当外部使用 from xx import *,引入的文件和函数
```

```python
__doc__
# 一个attribute,显示docstring
```

```python
# this is a module,not a atrribute
__future__
#就是把python大版本更新的内容带进来
```

```python
__docformat__
#让python文本转化器,知道docstring是按照什么方式写的
```

```python
__import__
#跟普通的import不同支持动态引入
for _dependency in _hard_dependcies
	__import__(_dependency)
```

