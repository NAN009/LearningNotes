#### String 提供构造管理字符串的基本逻辑；典型的不可变（Immutable）类,被声明为final class,所有属性也是final;
由于它不可变性，类似拼接、裁剪字符串都会产生新的String对象；大量数据操作时对性能有影响

#### StringBuffer 解决上述拼接产生中间对象问题的类；线程安全的可修改字符序列；保证了线程安全，故开销比StringBuilder大

#### StringBuilder 与StringBuffer无本质区别，不保证线程安全

####字符串缓存

日常开发中，字符串重复较多，避免创建重复，降低内存消耗和对象创建开销，
Java 6以后String提供intern()方法，提示jvm别相应支持费缓存起来以备复用。
G1 GC将字符串排重，将相同数据的字符串指向同一份数据。