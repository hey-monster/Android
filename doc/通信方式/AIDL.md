参考链接：
https://blog.csdn.net/luoyanglizi/article/details/51980630
https://www.jianshu.com/p/23612b2cce30

要使用AIDL，Service需要以aidl文件的方式提供服务接口，AIDL工具将生成一个相应的java接口，并且在生成的服务接口中包含一个功能调用的stub服务桩类。Service的实现类需要去继承这个stub服务桩类。Service的onBind方法会返回实现类的对象，之后你就可以使用它了。
交互过程client<-->proxy<-->stub<-->service
