# Python Learning #
## 1.data type ##
string,number,bool,dict,tuple,list
###dict:
Python的一种数据类型，类似于字典，以{key：value，...}形式存在。
一个key只能对应一个value，多次对一个key放入value时，后面的值会把前面的冲掉。
dict的key不存在时会报错，为了避免可以：

a.调用前用in判断key是否存在 

b.用dict的get()方法，自己决定返回值

    > d.get('Thomas')
    > d.get('Thomas', -1)
      -1

删除key：pop()
注意:dict内部存放的顺序和key放入的顺序是没有关系,dict的key必须是不可变对象，字符串，整数都是不变的，可作为key，list可变，不可作为key.

    > key = [1, 2, 3] 
    > d[key] = 'a list'
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: unhashable type: 'list'
###set
set和dict类似，但不存储value，因此set中的元素不重复

    > s = set([1, 1, 2, 2, 3, 3])
    > s
    set([1, 2, 3])
其中，[1,1,2,2,3,3]不表示一个list.

对于不变对象（如string）来说，调用对象自身的任意方法，也不会改变该对象自身的内容。相反，这些方法会创建新的对象并返回，这样，就保证了不可变对象本身永远是不可变的。

    > a = 'abc'
    > b = a.replace('a', 'A')
    > b
    'Abc'
    > a
    'abc'

###可变参数和不可变参数


