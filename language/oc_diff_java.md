
##<a name="table"/>oc is different from java
OC  | java
------------- | -------------
Objective-C使用消息传递（本质是字符串），因此方法、类和对象可以在运行时确定和修改  | Java的方法是与class静态绑定的，虽然可以在运行时用反射的机制获取，但效率会下降1个数量级
Objective-C会生成本地代码  | Java是编译成字节码，再通过JIT机制编译成本地代码
Smalltalk系：Objective-C、COM（非语言，但仍是编程系统）。特点是vtable/dispatch机制可以在运行时变化|Simula系：C++、Java、C#。特点是vtable在编译时确定.
动态语言Python、Ruby、JavaScript，则是Hash-table系的OO，特点是对象其实就是Hash-table|null
无命名空间|Java有package，命名空间
Objective-C是引用计数，发生在编译期|内存管理方面Java是垃圾回收，发生在运行时
Objective-C是动态语言，程序在运行时可以改变其结构：新的函数可以被引进，已有的函数可以被删除等在结构上的变化。比如众所周知的ECMAScript(JavaScript)便是一个动态语言。除此之外如Ruby、Python等也都属于动态语言，而C、C++等语言则不属于动态语言 | Java是静态语言，静态类型语言的类型判断是在运行前判断（如编译阶段），比如C#、java就是静态类型语言，静态类型语言为了达到多态会采取一些类型鉴别手段，如继承、接口
null|越是复杂的项目，使用静态语言可以利用编译器更早的发现和避免问题。
方法与参数命名遵照自然语义|null
第一次，通过CLang编译伪代码，伪机器码即Bticode 整理好业务逻辑前后顺序等，第二期，通过LLVM编译为机器码。OC/C/C++编译过程：OC、C、C++的源程序——前段工具CLang——代码对应的抽象语法树LLVM Bitcode——后端LLVM——机器语言|1、源文件由编译器编译成字节码（ByteCode）  2、字节码由java虚拟机解释运行。
object not responed|空指针异常
虽然Objective-C在语法上禁止类使用多继承,但是在协议的遵守上却允许使用多继承。所以可以用协议来实现多继承| java 不能多继承。只能单继承,但是可实现多接口
null | 同样的一个方法能够根据输入数据的不同，做出不同的处理，即方法的重载——有不同的参数列表（`静态多态性`）当子类继承自父类的相同方法，输入数据一样，但要做出有别于父类的响应时，你就要覆盖父类方法，即在子类中重写该方法——相同参数，不同实现（`动态多态性`）
[oop设计原则](oop_principle.md)| 在面向对象程序设计中，协变返回类型指的是子类中的成员函数的返回值类型不必严格等同于父类中被重写的成员函数的返回值类型，而可以是更 "狭窄" 的类型。Java 5.0添加了对协变返回类型的支持，即子类覆盖（即重写）基类方法时，返回的类型可以是基类方法返回类型的子类。协变返回类型允许返回更为具体的类型   `返回值协变和参数逆变` 函数f可以安全替换函数g，如果与函数g相比，函数f接受更一般的参数类型，返回更特化的结果类型
2015OC加入新特性Lightweight Generics 轻量级泛型，轻量是因为这是个纯编译器的语法支持（llvm 7.0）|支持泛型
没有JAVA中那种对抽象函数和接口的明确定义,多继承协议|null

