# PieceNote
日常记录
---

> windows bat 暂停
* 阻止cmd窗体一闪而过，方便查看错误信息
```
@echo off
......
pause
```
---
> Java生成类方法签名，JNI回调应用层时特别有用
* 首先Java类需编译生成class字节码
* cd到字节码所在目录
* 执行cmd： javap -s 类名(不需要加上.class)
* 控制台即会打印签名信息，如
```
Compiled from "JniParser.java"
public class com.gosuncn.libparser.jni.JniParser {
  public static com.gosuncn.libparser.jni.JniParser getInstance();
    descriptor: ()Lcom/gosuncn/libparser/jni/JniParser;

  public void responseDataCallBack(long, int, java.lang.String);
    descriptor: (JILjava/lang/String;)V

  public native long createParser();
    descriptor: ()J
    
    ...
}

```

---
> 移动数据统计、报告
* http://www.umeng.com/reports.html?from=hp
* https://mta.qq.com/mta/data/device
* https://www.zhihu.com/question/19766160

---
> iOS数据统计、报告
* https://developer.apple.com/support/app-store/
* https://david-smith.org/iosversionstats/
