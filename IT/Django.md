# Django
* Install Django on CentOS 7.0(use python 2.7)
```

>
```


```


```


```

```

```


```
```


```
```
使用``easy_install MySQL-python``，注意大小写

```

```



```
```
```

```
```

```

```
```

```
```

```
```


```
```




```
---------+---------+------+-----+---------+----------------+
---------+---------+------+-----+---------+----------------+
---------+---------+------+-----+---------+----------------+



```


```
```


```
----------------------------+----------------------+------+-----+---------+----------------+
----------------------------+----------------------+------+-----+---------+----------------+
----------------------------+----------------------+------+-----+---------+----------------+


```
```

```
pip install Pillow

>
```


```
```


```
Migrations for 'alltest':
```

```


```
----------------------------+----------------------+------+-----+---------+----------------+


对应表结构
```
----------------------------+----------------------+------+-----+---------+----------------+
----------------------------+----------------------+------+-----+---------+----------------+


```


```


```
```


```
```


```


```
```


```
```


```


```
models.ForeignKey(‘self’)
```

在views.py中引入

```


```
```

```


```
```


```


```


```

数据库里

```
----+------+------------+
----+------+------------+
----+------+------------+
----+-------+
----+-------+
----+-------+


```

```


```

```


```

```


```



```


```


```

```

```



```
```

```
```	
>这样post url http://domain/nocsrf将不会作csrf检查
```

```


```
```


---|---
has\_key()|检查request.GET or request.POST中是否包含参数指定的Key。
get\_full\_path()|返回包含查询字符串的请求路径。例如， "/music/bands/the_beatles/?print=true"

---|---
items()|和标准字典的items()方法有一点不同,该方法使用单值逻辑的\_\_getitem\_\_():
values()|和标准字典的values()方法有一点不同,该方法使用单值逻辑的\_\_getitem\_\_():

update() 例子

```
```

items() 例子

```
```

---|---
urlencode()|返回一个以查询字符串格式进行格式化后的字符串(e.g., "a=2&b=3&b=5").

lists() 例子

```
```


```
```


```
```



```


---|---

```

return HttpResponseNotFound('<h1>Page not found</h1>')
```
```
    


```
```


```
```



```

```
```


```


```

```


```
```
```


```
```

```
```


```
```


```





```


```

```
```



```

```

```


```



```

```



```
```

```


```
---|---|---

```


```

```

```


<img src="{% static "test/test.jpg" %}" alt="My image">
```

```


```
```

```
```


```

```
```

```


```


```


```

``from django.db.models import Q``


```


```


```

动态获得Q对象

```
direct_comment = _tasks.filter(user=F('assigned_user'))
```

```


```
```


保存到数据库，方法没有返回值

在后台执行了 UPDATE 这一SQL语句
当你从数据库中获取对象的时候，你实际上用 Manager 模块构造了一个 QuerySet ，这个 QuerySet 知道怎样去执行SQL语句并返回你想要的对象。

用 filter() 和 exclude() 方法可以实现这样的功能

``` 


```


``` 


```


```


```

```


```

```

```
 




```


```

```





```


```

>>>Blog.objects.filter(name__endswith='Blog') 


```



```



```
```
  
>如果一个源模型含有一个外键,那么它的外键模型的实例,可以利用”Manager”返回这个源模型的所有实例.默认的这个”Manager”叫做”FOO_set”,这个”FOO”是源模型的名字,小写字母,这个”Manager”将返回”QuerySets”,对这个QuerySets进行过滤和操作,就像在检索对象章节中介绍的.  

```

>当你在 model 中定义了一个关系字段(也就是,一个ForeignKey, OneToOneField, 或 ManyToManyField). Django 使用关系字段的名字为 model 的每个实例添加一个描述符. 在访问对象或关联对象时, 这个描述符就象一个常规属性. 
>举例来说, mychoice.poll 会返回 Choice 实例对象关联的 Poll 对象.  通过下面的关系,连接可以以非显式的方式进行: ``choices.objects.filter(poll__slug="eggs") ``得到一个 Choice 对象列表, 这些对象关联的 Poll 对象的 slug 字段值为 eggs. 允许多级连接.  通过一个对象实例的便利函数(convenience functions)就可直接查询该对象的关联对象. 举例来说, 如果 p 是一个 Poll 实例, p.choice_set() 将返回所有关联的 Choice 对象列表. 聪明的读者会注意到它等价于 ``choices.objects.filter(poll__id=p.id)``, 只是更加清晰.  每一种关系类型会为关系中的每个对象自动创建一系列便利方法(类似 ``choice_set()`` 这样的方法).这些方法被双向创建, 这样被关联的对象就不需要明确的定义反向关系, 这一切都是自动完成的.  

```

```
>在多对多关系的两端，都可以通过相应的API来访问另外的一端。 API的工作方式跟前一节所描述的反向一对多关系差不多。唯一的不同在于属性的命名：定义了``ManyToManyField``的model的实例使用属性名称本身，另外一端的model的实例则使用model名称的小写加上``_set``来活得关联的对象集（就跟反向一对多关系一样）

```

>设置字段隐藏值，如：性别，M=Male，F=Female 
```

```

```

>不存在 null=True 的每个 DateField 和 DateTimeField 自动拥有 get_next_by_FOO() 和 get_previous_by_FOO() 方法, 此处的 FOO 是字段的名字. 它们分别返回该字段的上一个对象和下一个对象. 如果上一对象或下一对象不存在,则抛出 *DoesNotExist 异常. 这两个方法均接受可选关键字参数, 这些参数应该遵循上文中 "Field 查询" 中提到的格式.  注意如果遇到相同值的对象, 这些方法会使用 ID 字段进行检查. 这保证了没有一条记录会被跳过或重复记数.参阅 lookup API sample model_ ,那里有一个完整的例子. 
>对一个 FileField 对象来说, 它自动拥有一个 get_FOO_filename() 方法. 这里 FOO 是字段名,它根据你的 MEDIA_ROOT 设置返回一个完整的路径名称.  注意 ImageField 技术上是 FileField 的一个子类, 因此每个有 ImageField 的 model 自动拥有此方法. 
>含有 FileField 字段的每个对象自动拥有一个 get_FOO_url() 方法,这里的 FOO 是字段的名字. 该方法根据你的 MEDIA_URL 设置返回该文件的完整 URL ,如果 MEDIA_URL 设置为空, 该方法返回一个空的字符串. 
>含有 FileField 字段的每个对象自动拥有一个 get_FOO_filename() 方法, 这里的 FOO 是字段的名字. 该方法返回文件的长度(字节数).(在后台, Django 使用 os.path.getsize.)  
>含有 FileField 字段的每个对象自动拥有一个 get_FOO_filename() 方法, 这里的 FOO 是字段的名字. 该方法使用给定的文件名将文件保存到文件系统.. 如果同目录下已经有同名文件存在,Django 会在文件名后添加一个下划线(扩展名之前)直到文件名有效为止(也就是如果加了下划线还重名,就再加....直到没有重名为止). 
>含有 ImageField 字段的每个对象自动拥有 get_FOO_height() 和 get_FOO_width() 方法, 这里的 FOO 是字段的名字. 它们返回相应的图片高度和宽度(整数,以像素计).

```



```


```

```

```






```        
```        
        

```
teacher.student_set.all()

```

```

```


```



```



```


```


```
```



```

```

url(r'^snippets/(?P<pk>[0-9]+)/$', views.snippet_detail),
```

```

django shell 里使用


```


```




```
