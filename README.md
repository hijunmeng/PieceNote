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
> 批处理文件模板
* 由于bat嵌套调用时并不会切换到目标bat的目录，因此需要先切换到bat所在的目录下再执行
```
set cdir=%~dp0
set wdir=%cd%
cd /d %cdir%
rem "将下面的 %startup.bat% 改为真正要启动的bat文件，或者命令”
%startup.bat%
cd /d %wdir%
```
```
比如你有个批处理a.bat在D:\qq文件夹下 
a.bat内容为 
cd /d %~dp0 
在这里 
cd /d %~dp0的意思就是cd /d d:\qq 
%0代表批处理本身 d:\qq\a.bat 
~dp是变量扩充 
d既是扩充到分区号 d: 
p就是扩充到路径 \qq 
dp就是扩充到分区号路径 d:\qq
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
