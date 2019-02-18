# Spring学习

## Spring概念

* Spring是开源轻量级框架



* Spring的两个核心

  * aop:面向切面编程,扩展功能不是修改源代码实现

  * ioc:控制反转

    常规调用一个不是静态方法的类时,需要new出对象然后调用,创建对象过程需要new出对象;

    而在Spring中对象的创建不是通过new方式实现,而是通过Spring中的配置创建类的对象

    

* Spring是一站式框架

  * Spring在javaee三层结构中,每一层都提供不同解决技术

    * web层:Spring MVC

    * Service层: spring的ioc

    * dao层: spring的jdbcTemplate

      

* spring版本

  * hibernate
  * spring

## Spring的ioc操作

* 把对象的创建交给Spring进行管理
* ioc操作两部分
  * ioc的配置文件方式
  * ioc的注解方式

## ioc的底层原理

* ioc底层原理使用技术

  * xml配置文件
  * dom4j解决xml
  * 工厂设计模式
  * 反射


## Bean标签常用属性

* id属性
  * 作用:名称
  * id属性值名称任意命名
  * 不能包含特殊符号
  * 在代码中根据id值得到配置对象

* class属性
  * 创建对象所在类的全路径
* name属性
  * 功能和id熟悉一样
  * name属性值里面可以包含特殊符号
* scope属性
  * singleton : 默认值,单例
  * prototype:多例
  * request:创建对象放在request域里
  * session:创建对象放在session域里
  * globalsession:创建对象把对象放在globalSession里面



