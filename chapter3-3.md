###reactor
#####reactor是twisted的event循环，也是整个app的驱动。reactor提供许多在线程，网络，事件等api。

1.run
  reactor.run()，启动reactor事件循环
  
2.stop
  对应的,停止事件循环
  
3.running
  判断当前reactor是否正在运行，如果是则返回True，否则为False
  
4.addSystemEventTrigger（phase, eventType, callable, *args, **kw）

  当system事件发生的时候，执行添加的function。系统事件，比如start,stop等。通常呢，我们用做在服务器关闭的时候，
  添加一些函数，用来处理数据入库等操作，保证服务器关闭的时候，内存数据不会丢失。
  
  
  
  
5.removeSystemEventTrigger
6.callWhenRunning