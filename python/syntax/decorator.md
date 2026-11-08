***

*describe*：

​	decorator是一个能修改其他函数功能的函数，让代码更简单，更pythonic。

***

需要提前理解的几个basic：

...省略号语法,任意参数任意内容[ellipsis语法]

### 一切皆为对象

函数也可以是对象，可以进行复制

```python
def hi():
	print("hi,mr.abram")

greet = hi

greet()
```

greet函数也可以调用了。

### 函数中也可以返回函数

```python
def hi(name="abram"):
	def greet():
		return print("It's a greet hornor to meet you.")
	def hello():
        return print("It's a hornor to meet you.")
    if name=="abram":
		return hello
    else:
        return greet
```



###  函数内部可以定义函数

```python
def hi():
	def greet():
		print("greetings,my load")
		
	def hello():
		print("Sir,It's an hornor to meet you.")
	greet()
	hello()
```

###　函数可以作为参数传入

```python
def hi(func):
	def greet():
		print("greetings,my load.")
	
    def hello():
    	print("Sir,It's an hornor to meet you.")
    
    hello()
    func()
    greet()
def	abram():
    print("hello,abram.")

hi(abram)
```

什么是一个decorater呢

就是一个简化,如果我们希望这个函数是经过另外一个函数包装之后的函数,或者我们每次call这个函数的时候需要她被包装一下.

```python
from functool import wraps
def func(_func):
    @wraps(_func)
	def func1():
		print("dear abram,you are my holly load.")
		_func()
	return func1
@func
def abram():
	print("abram,you are my one truly god.Live long and prosper.")

#lord = func(abram)简写就是转化为,上面的.
```

