# SpringMVCDemo

This is just a demo for learning

 Android Studio  |   JDK   |   tomcat   |   SQLServer   
:----------------|:--------|:-----------|:--------------
      2.3.x      |  1.8.x  |    7.0.x   |     2012




## Notes （ [学习时参考的文章链接](https://my.oschina.net/gaussik/blog?sort=time&temp=1512221097893) ）

1. [数据库的链接配置的问题](http://blog.csdn.net/qac_boy/article/details/75529153)

2. 在 《使用IntelliJ IDEA开发SpringMVC网站（三）数据库配置》 中；需要修改的地方有
在 **UserEntity.java** 中：
@Table(name = "user"...);
**name = "user" 修改为 "[user]" ( ps: user 表名是系统的 )**
即为： @Table(name = "[user]"...);

3. 报错：“ 当 IDENTITY_INSERT 设置为 OFF 时，不能为表 'user' 中的标识列插入显式值 ”（在 BlogEntity.java 中也是一样）
[解决问题参考链接](http://blog.csdn.net/itmyhome1990/article/details/7460378)
在 @Id 下
加入 **@GeneratedValue(strategy=GenerationType.IDENTITY)**
