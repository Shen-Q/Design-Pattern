# Design-Pattern

>## 创建型：
>* 单例模式  `保证只存在一个对象实例` <br>
>       ### 饿汉式——静态常量<br>
>       特点：构造器私有化、加载时创建对象`final` `static`、取出的实例相等<br>
>       缺点：易造成内存浪费，可能没有用到的时候加载了类就实例化了
>```java
>Class Singleton{
>   private final static Singleton instance = new Singleton();
>   private Singleton(){ }
>   public static Singleton getInstance(){ return instance; }
>}
>
>
>       ### 饿汉式——静态代码块<br>
>           缺点同上
>```java
>Class Singleton{
>   private static Singleton instance;   
>   private Singleton(){ }
>   static {
>       instance = new Singleton();
>   }
>   public static Singleton getInstance(){ return instance; }
>}
>
>
>       ### 懒汉式——线程不安全<br>
>           特点：调用 getInstance() 方法时才创建实例
>```java
>Class Singleton{
>   private static Singleton instance;   
>   private Singleton(){ }
>   public static Singleton getInstance(){ 
>       if(instance==null){     //调用方法后，第一次判断instance为空时才创建实例。否则直接返回instance
>           instance = new Singleton(); //线程不安全，如果有两个线程同时在判断是否为null
>       }
>   return instance;
>   }
>}

>* 抽象工厂
>* 原型模式
>* 建造者模式
>* 工厂模式

>结构型：



>行为型：
    
