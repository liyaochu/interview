# interview
# java 面试精选
##基础篇
###基本功
####1.面向对象的特征
**面向对象的编程语言有封装、继承 、抽象、多态等4个主要的特征。**
https://www.cnblogs.com/guweiwei/p/6599289.html
####2.final, finally, finalize 的区别
**final是修饰符，修饰类、方法和变量，意为不可修改的。当修饰类的时候不可以派生出新的子类，因此一个类的修饰符不可以既是final和abstract；修饰方法的时候该方法不可以被重载；修饰变量的时候需要给变量赋初值，在接下来只能对其读取不可以重新赋值。**

**finally是在异常处理时提供finally块来执行任何清除操作的，如果try语句中发生了catch块中的异常，则跳转到catch中进行异常处理，而finally中的内容则是无论异常是否发生都要执行的。如果finally中有return，则会先执行finally再执行return，如果此时try中也有return，则try中的return不会执行，但是，如果只有try中有return也是先执行finally中的语句再执行return；**

**finalize是方法名，在垃圾回收器将对象从内存中清理出去之前做的必要工作。是由垃圾回收器在确定这个对象没有被引用的时候调用的，它是在Object中定义的，子类重写finalize方法整理系统资源或其他清理工作finalize方法是在垃圾收集器删除对象之前调用的。**
####3.int 和 Integer 有什么区别
**1、Integer是int的包装类，int则是java的一种基本数据类型** 

**2、Integer变量必须实例化后才能使用，而int变量不需要** 

**3、Integer实际是对象的引用，当new一个Integer时，实际上是生成一个指针指向此对象；而int则是直接存储数据值 。**

**4、Integer的默认值是null，int的默认值是0**
####4.重载和重写的区别
**重写:从字面上看，重写就是 重新写一遍的意思。其实就是在子类中把父类本身有的方法重新写一遍。子类继承了父类原有的方法，但有时子类并不想原封不动的继承父类中的某个方法，所以在方法名，参数列表，返回类型(除过子类中方法的返回值是父类中方法返回值的子类时)都相同的情况下， 对方法体进行修改或重写，这就是重写**
**重载:在一个类中，同名的方法如果有不同的参数列表（参数类型不同、参数个数不同甚至是参数顺序不同）则视为重载。同时，重载对返回类型没有要求，可以相同也可以不同，但不能通过返回类型是否相同来判断重载**
####5.java中==和eqauls()的区别
**==是运算符,用于比较两个变量是否相等,而equals是Object类的方法,用于比较两个对象是否相等.默认Object类的equals方法是比较两个对象的地址,此时和==的结果一样.换句话说:基本类型比较用==,比较的是他们的值.默认下,对象用==比较时,比较的是内存地址,如果需要比较对象内容,需要重写equal方法**

###集合
####1.List 和 Set 区别
**1、List,Set都是继承自Collection接口**
**2、List特点：元素有放入顺序，元素可重复 ，Set特点：元素无放入顺序，元素不可重复，重复元素会覆盖掉，（元素虽然无放入顺序，但是元素在set中的位置是有该元素的HashCode决定的，其位置其实是固定的，加入Set 的Object必须定义equals()方法 ，另外list支持for循环，也就是通过下标来遍历，也可以用迭代器，但是set只能用迭代，因为他无序，无法用下标来取得想要的值。**
**3.Set和List对比：** 
**Set：检索元素效率低下，删除和插入效率高，插入和删除不会引起元素位置改变。** 
**List：和数组类似，List可以动态增长，查找元素效率高，插入删除元素效率低，因为会引起其他元素位置改变。** 

####2.List 和 Map 区别
**List是存储单列数据的集合，Map是存储键和值这样的双列数据的集合，**

**List中存储的数据是有顺序，并且允许重复；**

**Map中存储的数据是没有顺序的，键不能重复，值是可以有重复的**
####3.Arraylist 与 LinkedList 区别
**1.ArrayList是实现了基于动态数组的数据结构，LinkedList基于链表的数据结构。 （LinkedList是双向链表，有next也有previous）**
**2.对于随机访问get和set，ArrayList觉得优于LinkedList，因为LinkedList要移动指针。** 
**3.对于新增和删除操作add和remove，LinedList比较占优势，因为ArrayList要移动数据。**
####4.ArrayList 与 Vector 区别
**1）  Vector的方法都是同步的(Synchronized),是线程安全的(thread-safe)，而ArrayList的方法不是，由于线程的同步必然要影响性能，因此,ArrayList的性能比Vector好。** 
**2） 当Vector或ArrayList中的元素超过它的初始大小时,Vector会将它的容量翻倍,而ArrayList只增加50%的大小，这样,ArrayList就有利于节约内存空间。**
####5.HashMap 和 Hashtable 的区别
https://blog.csdn.net/qq_28081081/article/details/80613460
####6.HashSet 和 HashMap 区别
http://www.importnew.com/6931.html
####7.HashMap 和 ConcurrentHashMap 的区别
http://www.importnew.com/28263.html

####8.HashMap 的工作原理及代码实现
https://www.cnblogs.com/chengxiao/p/6059914.html
####9.ConcurrentHashMap 的工作原理及代码实现
https://www.cnblogs.com/chengxiao/p/6842045.html

