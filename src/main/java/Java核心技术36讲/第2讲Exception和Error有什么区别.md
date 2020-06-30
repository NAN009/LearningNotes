##请对比Exception和Error，运行时异常与一般异常区别

####共性：
* 都继承Throwable类，只有该类型的实例可以被抛出、捕获，是异常处理机制的基本类型
####差异：
* Error指的是正常情况下不太可能出现的情况，大部分Error都会导致程序不可恢复，不需要捕获，比如OutOfMemoryError
* Exception分为可检查（checked）异常和不检查（unchecked）异常；可检查异常必须在代码中显式捕获，编译期检查，如IOException。
不检查就是运行时异常，如NullPointerException，编译期不要求捕获



1、尽量不要捕获类似Exception这种通用异常，尽量捕获特定异常
   
    说明：更直观体现异常信息

2、不要生吞异常
       
    说明：把异常抛出活输出到日志，方面问题排查
    
