USER类的定义及其子类

父类   USER类  抽象类   

子类     Visitor    游客    

​	    ADM     管理员

​	    Signer   用户 (非游客用户)

```c
// 1,   3个类的声明
```

  	   三个子类均采用标准的java Bean方式编写  \

```c
// 2 有多参数构造方法的声明和调用；
```

​      抽象一个叫做Signin的接口     ,接口中定义的方法有

```python
#1    searchUser   在对应的数据库中寻找用户,返回对应的json字符串
#2    setUser      用户想要更改信息,就要把他们的信息写入到对应的数据库里面
#3    addUser      如果是新用户,就要把他们的信息写入到对应的数据库里面
#4    delUser      删除用户 

#因为我还没有学到整合mybatis ,所以大家的数据库目前暂定就是一个csv文件而已,实现的时候接受的对象是一个json的字符串,具体的这个json字符串的定义形式我们讨论一下再决定吧
```

```python
#3、抽象至少一个接口，接口中至少有3个以上的方法，并在类中实现；
```

在写这三个子类定义的时候肯定会有方法、变量、常量的声明和调用的,而且这个实际上也很类似的啦

```python
#eg  先写一下我想到的,到时候再说再添
成员变量
int   id   唯一识别 取6位  首位以权限开头 不准重复
  int 权限  0 1 2   越大权利越大   
  int  年龄    
  int  性别  0 是男   1 是女
  String   nickname
  String  密码   8到12位 只能用英语的大小写字母he数字
  先这样,不够到时候再添
```

```c
//4、有方法、变量、常量的声明和调用；

//5、至少有三种控制结构的使用；

//6、有类的继承；

```





不是特别肯定的东西 

```
7、有final关键字、访问控制符的使用，访问控制符至少有三种以上的使用；
```

除开常量之外 ,我们应该可以final 一个root用户

final 一个  标准的错误用户的定义(比如我查不到注册用户,那么不要出错,查不到就返回一个标准的错误用户的json字符串给我)



```
8、程序中体现三个线程的并发；
```

这主要是我的任务,多线程并发处理请求,和嗯 ,类的定义关系不大

```
9、使用throw抛出自定义异常。
```

增删改查出问题的时候可以这样,处理方式是返回一个标准的错误用户的json字符串

```
10、至少有3个以上界面，界面之间能够联动，完善界面功能的事件处理，事件处理三个以上，能够通过界面进入主程序，并调用其他界面，以及完成事件处理。软件运行的界面截图，其中是GUI编程的，给出GUI运行后的结果截图，如果没有设计GUI编程的代码，给出dos界面运行结果截图
```

