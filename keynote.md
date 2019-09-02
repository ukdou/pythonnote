#### Python基础知识

1. ##### a的赋值，= 与 ==
	```python
	a=2 给a赋值为2
	print(a), result为2
	print(a==2), 是在判断现在a的值是否为2，反馈的result为 Bool: True /False
	print(a=2), 相当于print(write(a,2)),是在判断将2写入a这个动作是否成功，反馈的result为 Bool: True /False	
	```

2. ##### dictionay 字典
	keys和values是有唯一的对应关系，一个key只对对应的value负责
	```python
	d {} # create a blank mapping, mapping like a table, has keys and values
	keys() # like a title column in a table. key可以是数字也可以是字符串
	values()# the 与keys对应的 value within a mapping
	```
	get an element from a dict using these [] brackets, not these ()
	```python
	d=dict() #建一个空字典
	```
	```python
	d = {'apple':1,'pear':2}
		del d['pear'] 删除现有字典里的元素
	```
	如果需要加入元素，直接定义
	```python
	d['b'] = 20
	```
	字典中可再嵌入字典或者列表
	```python
	d = {'apple':[1,2,3,4], 'pear':{1:3, 3:'a'}，'orange':3}
		print(d['pear'][3]) #打印pear下的3这个key对应的值
	```
	字典不会按照序列自动排序，list是按照顺序的容器
	<br>
3. 
	##### def 函数
	function是一种功能和逻辑， A和B为影响该逻辑的参数
	```python
	function(A, B)
	def function(A, B) 是给逻辑和参数的命名和定义, 并调用A和B做逻辑运算
	```
    <br>
4. 
	##### index 
	index 是指一个字符串或者数字中某一个值的序列/位置，意义说是泛指index; 当字符串中出现同样的char时， 会依次继续进行i+1
	index()功能，会在出现相同的char的时候，给出‘第一次’出现该值时，出现的i
	定义i的范围
	range(len(字符串/数值，字符串/数值))，若只有一个参数，则默认从0开始
    <br>
5. 
	##### 循环
	For x in y 循环 和if,else 需要在使用时用':' 结尾
	While 循环， 只当while后面的条件成立后(True)，才进入循环
    <br>
6. 
	##### Array
	一组数值like [-2, 1, 0, 2, 5, 7, 9]
	A组数列中，第一个值得序列为0，最后一个数值的序列为 len(A)-1
    <br>
7. 
	##### 字符串与字符
	String & Char
    <br>
8. 
	glocal全局变量定义
	Local局部变量定义
    <br>
9. 
	##### 读写文件
	open('文件名称'，'打开形式')；
	1. 在还未有此文件时，会自动生成该命名文件；
	2. 打开形式：r-read; w-write; a-append; r+(open for reading and writing); a+ (open forreading and appending, writing at the end of the file); +b (binary二进制)
	```python
	.write()写入
	.read()读取内容
	.readline()-读第一行
	.readlines()-读所有行 以list的形式读取，并存储到Python的list中[a,b,c,d,...]， 可用来读取excel
	.close()关闭文件 
	```
	\n ：想在text中换一行，可在中间加\n
	<br>
10. 
	##### class 类
	定义一个class，一般开头字母大写,如 
    ```python
	class Calculator:
		name = 'My Good Calculator' 类的默认属性
		price = 18 类的属性
		def add(self,x,y): 类的功能，self为自带的参数，可用来展示类的属性
			print(self.name)
			result = x+y
			print(result)
    ```
	定义好类后，可运行这个类
	可先定义一个自变量等于这个类，然后再调用设定好的类，如
    ```python
	cal = calculator()
	这样当需要调用该类的属性/功能时，则可以直接调用，如
	Cal.name  /  Cal.price 会运行后得出，'My Good Calculator' 和 18
	Cal.add(10,11) 会运行后得出，21
	```
	init 类的初始，生成类的时候，初始定义
	如果需要自己定义属性，可用init, 但同时也可以设置默认值
    ```python
	def_init_(self, name, price, height, width):
		self.n = name
		self.p = price
		self.w = width
		self.h = height
    ```
	想先设置默认值时def_init_(self, name, price=18, height=10, width=20):
	调用时，可直接Cal.n / Cal.p
    <br>
11. 
	##### Input
	input输出的结果为字符串string
	<br>	
12. 
	##### tuple & list 元组合列表
    ```python
	a_tuple = (1,2,3,22,45)也可以无括号
	a_list = [1,2,3,22,45]   
    ```
	<u>List:</u> 
    a = [1,2,3,4,5,2,1]
	a.append(0) 在list a 的最后追加一个为0的值
    
	```python
	a = [1,2,3,4,5] # 线性列表
	```
	```python
	multi_dim_a = [[1,2,3],
		       [2,3,4],
		       [3,4,5]]
	#多维列表
	```
	打印时：
	```python
	print(a[1]) 
	print(multi_dim_a[0(行数)][1(列数)])
	```
	<br>

13. 
	##### import 引入模块
	```python
	import time/ import time as t
	time.localtime() / t.localtime()
	```
	如果只想从time调用某几个功能
	```python
	from time import localtime, B, C
	调用时，可直接使用 localtime(), B(), C()
	```
	引用time下的所有功能
	```python
	from time import*
	调用时，可直接使用 localtime(), B(), C()
	```

	可import同文件夹目录下的其他Python文件中的功能模块
	<br>

14. 
	##### continue & break 
	是循环中的两个重要的继续或者跳过的方法
	若不使用continue/break, 当a成立进入循环，如果b的值为2，a则赋值为False,则跳出循环

	```python
	a = True
	while a:
		b = int(input('guess my numbers'))
		if b = 2:
			a = False
		else:
			pass
	```
	若使用 break
	```python 
	while True:
		b = int(input('guess my numbers'))
		if b = 2:
			break # 当b=2时,不循环下面print('still in while')的语句,直接打印finish
		else:
			pass
		print('still in while')
	print('finish')
	```
	若使用 continue
	```python 
	while True:
		b = int(input('guess my numbers'))
		if b = 2:
			continue # 当 b=2时,直接跳回while循环语句中，忽略后面所有的语句
		else:
			pass
		print('still in while')
	print('finish')
	```
	<br>


15. ##### 异常处理
	例子：尝试打开一个不存在的文件
	```python
	try:
		file = open('doudou','r+') # 尝试打开名为‘doudou’的文件，并读取
	except Exception as e: # 若尝试出现异常(例外)，将Exception(常规类异常)存为 e 
		print(e) # 打印异常
		print('there is no file named as doudou')
		response = input('do you want to create this file?')
		if response = 'yes'
			file = open ('doudou','w') # 生成名为doudou的文件，并以写入的方式打开
		else
			pass
	else
		file.write('hello') # 若成功打开并无议程，在文件内写入hello
	file.close
	```
16. ##### zip, lambda, map
	<u>Zip</u>
	有两个列表元素a和b
	```python
	a = [1,2,3]
	b = [4,5,6]
	```
	如果用 zip 将 a和b 合并
	```python 
	zip(a,b) # 这样返回的是一个object代码
	list(zip(a,b)) # 如果要可视zip(a,b)，则需要展示为列表list
		得到 [(1,4),(2,5),(3,6)]
	```
	如果需要同时对a和b进行运算，并合并
	```python
	for i, j in zip (a,b): 对于a和b列表里的i值与j值
		print(i/2, j*2)
		得到 
		0.5 8
		1.0 10
		1.5 12
	这是将两个元素zip起来运算的的结果
	```
	zip 支持 合并多个元素，如 
	```python 
	list(zip (a,b,b))
		得到 [(1,4,4,),(2,5,5),(3,6,6)]
	```
	<u>lambda</u>
	lambda主要用来定义简单的方程语句
	正常用define定义功能时：
	```python
	def function1(x,y)
		return(x+y)
	```
	当用 lambda 达到相同功能时：(lambda 元素:功能)
	```python
	function1 = lambda x,y:x+y 
	```
	<u>map</u>
	map(function(), list1[ ], list2[ ])
	```python
	def fucntion1(x,y)
		return(x+y)
	map(fucntion1, [1], [2])  # 和zip相同，这样返回的是一个object代码
	list(map(fucntion1, [1], [2])) # 如果要可视 map，则需要展示为列表list
		得到 [3]
	```
	map 支持多参数运算
	```python 
	map(fucntion1, [1,2],[10,11])
	list(map(fucntion1, [1,2],[5,22]))
		得到 [6,24]	
	```
	<br>
17. ##### copy & deep copy 
	值的复制可分为三种

	1. 新建变量，让变量b等于变量a，但b和a中的值会互相影响并保持一致
	2. 浅复制 copy.copy() , 第一层列表会被储存到不一样的空间（不会互相影响），但第二层列表中的值仍然会互相影响并保持一致
	3. 深复制 copy.deepcopy(), 会完全复制（无论第几层），并被储存到不一样的空间（不会互相影响）
	
	下面对以上三种情况进行简单的举例:
	<u>新建变量</u>
	```python
	a = [1,2,3,[8,9]]
	b = a 
	a = [11,22,3,[88,9]]
	print(b)
		得到[11,22,3,[88,9]]
	id(a) == id(b)
		True
	```
	<u>浅复制 copy.copy()</u>
	```python
	import copy
	a = [1,2,3,[8,9]]
	c = copy.copy(a)
	a = [11,22,3,[88,9]]
	print(c)
		得到[1,2,3,[88,9]]
	id(a) == id(c)
		False
	id(a[3]) == id(c[3])
		True
	```
	<u>深复制 copy.deepcopy()</u>
	```python
	import copy
	a = [1,2,3,[8,9]]
	d = copy.copy(a)
	a = [11,22,3,[88,9]]
	print(d)
		得到[1,2,3,[8,9]]
	id(a) == id(d)
		False
	id(a[3]) == id(d[3])
		False
	```
	<br>
18. ##### Pickle模块
	pickle可用来保存/提取python运算完的结果, 字典，变量，列表等
	```python
	import pickle

	d ={'a':111, 2:[33,4,5],'67':{99:10,'s'='sad'}}

	file = open('pickleexample.pickle','wb')
	pickle.dump(d,file) # 将d的结果取出，倒进file

	file.close() # 保存并关闭文件

	想要读取时， 存为字典d2
	with open('pickleexample.pickle','rb') as file：
		d2 = pickle.load(file)
	```
	<br>
19. ##### Set
	在列表中找不同，去重
	```python
	char_list = ['a','b','b','c','c','d']
	unique_char = set(char_list())
	print(unique_char)
		{'a','b','c','d'} # 返回一个class为 set 的结果
	
	unique_char.add('x') # 只能加 一个值，不可以加 list
	print(unique_char)
		{'a','b','c','d','x'} 
	
	unique_char.clear('a') 
	print(unique_char)
		set() # 返回一个空 set()

	unique_char.discard('a') 
	print(unique_char)
		{'b','c','d','x'} 	

	unique_char.remove('y') 
	print(unique_char)
		会因'y'不存在而报错， .discard不会
	```
	对两个set进行比对，
	```python
	setA = set(char_list())
	setB = {'a','e','i'}
	```
	找出不同：A 有 B 没有的唯一值
	```python
	print(setA.difference(setB))
		{'b','c','d'} 
	```
	找出相同：A 有 B 也有的唯一值
	```python
	print(setA.intersection(setB))
		{'a'} 
	```
	<br>
20. #### 正则表达式 regular expression (RegEx)
	对文本处理的强大武器,是用来匹配字符的一种工具，在一大串字符中找到所需内容。在python中通过导入 re 的模块引用正则表达式的功
	```python

	pattern1 = 'cat'
	pattern2 = 'bird'
	string = 'dog runs to cat'

	判断pattern是否在string中
	```
	<u>简单python匹配</u>
	```python
	# matching string
	print(pattern1 in string)
		True
	print(pattern2 in string)
		False
	```
	<u>用正则表达式寻找配对</u>
	```python
	# regular expression
	import re
	print(re.search(pattern1, string))
		<object>
	print(re.search(pattern2, string))
		None
	```
	<u>匹配多种可能 [ ] </u>
	```python
	# multiple ('ran' or 'run')
	import re
	pattern = r"r[au]n" # r 代表“”中是表达式而不是单纯的值，使用 [] 包含多种可能
	print(re.search(pattern, string))
		<object>
	```
	可以将 [ ] 中的内容设置为更多种
	```python
	一般字符/数字：
	[A-Z] | [a-z] | [0-9] | [0-9a-z]
	
	特殊种类：
	\d = 所有数字，包含小数点				
	\D = 所有非数字和小数点的值
	\s = 所有空白字符 [\t\n\r\f\v] ; \t (Tab 制表符) 、 \r (回车符)、\n (换行符) 和 \f (换页符) 
	\b = 相当于设定字符的前后都需要有 单个的 空格，如 r"\brun\b"
	\B = 相当于设定字符的前后都需要有空格
	()? = 可能存在也可能不存在的值放在括号里，如 r"Mon(day)?"
	^ = 判断是否在句首 r"^ dog"
	$ = 判断是否在句尾 r"cat$"
	. = 所有
	```
	如果是多个句子需要做匹配的判断，如需要判断每个句子的句尾/句首，则可以用 flags=re.M, M 表示multiple lines多行
	```python 
	string = """ dog runs to cat.
	cat runs to mouse.
	"""
	print (re.search(r"^cat", string)
		None
	print (re.search(r"^cat", string, flags=re.M))
		<object>
	```
	字符出现的次数：0次或者多次；1次或者多次; 或自定义次数
	```python 
	occur 0 or more times  *
	print(re.reserch(r"ab*","a"))
		<object>
	print(re.reserch(r"ab*","abbbbb"))
		<object>
	```

	```python 
	occur 1 or more times  +
	print(re.reserch(r"ab+","a"))
		None
	print(re.reserch(r"ab+","abbbbb"))
		<object>
	```
	```python 
	occur n to m times  {}
	print(re.reserch(r"ab{2,10}","a"))
		None
	print(re.reserch(r"ab{2,10}","abbbbb"))
		<object>
	```
	<u>寻找出所有匹配的值/字符串</u> re.findall()
	```python 
	# findall
	print(re.findall(r"r[au]n","run ran ren"))
		['ran','run']
	# or
	print(re.findall(r"ran|run","run ran ren"))
		['ran','run']
	```
	<u>替换匹配到的值/字符串</u> re.sub()
	```python 
	# replace value/string(char)
	print(re.sub(r"r[au]n",'jumps',"dog runs to cat"))
		'dog jumps to cat'

	```	
	<u>分裂</u> re.split()
	```python 
	# seperate
	print(re.split(r"r[,\.;]","a,b.c;d/e")) 因为'.'代表了任何东西， 所以要反斜杠'\' 去除该功能
		['a','b','c','d','e']
	```

	<br>

	











