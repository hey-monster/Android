Intent:即意图，一般是用来启动新的Activity，按照启动方式分为两类：显式Intent 和 隐式Intent

显示Intent就是直接以“类名称”来指定要启动哪一个Activity：Intent intent = new Intent(this , activity.class);　　其中activity.class就是要指定启动的activity

举个例子：新建有两个Activity：MainActivity 和 DemoActivity，现在从MainActivity跳转到DemoActivity



参考：
https://www.cnblogs.com/chenxd/p/7819251.html
