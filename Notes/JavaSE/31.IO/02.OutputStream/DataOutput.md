# DataOutput

```java
public interface DataOutput {}
```

DataOutput 接口提供了将数据从任何Java原语类型转换为一系列字节并将这些字节写入二进制流的功能。还有一种将字符串转换为修改后的UTF-8格式并写入结果字节序列的工具。

对于这个接口中所有写字节的方法，如果一个字节由于任何原因不能被写，通常会抛出一个IOException。

## 常用方法

```text
void write(byte[] b)
// 将字节数组中所有字节写入输出流
void write(byte[] b, int off, int len)
// 将字节数组中从 off 开始的 len 个字节写入输出流
void write(int b)
// 将字节写入输出流
void writeBoolean(boolean v)
// 将布尔值写入输出流
void writeByte(int v)
// 将参数字节的八个低位写入输出流
void writeBytes(String s)
// 将字符串写入输出流
void writeChar(int v)
// 将由两个字节组成的字符值写入输出流。
void writeChars(String s)
// 将字符串s中的每个字符按每个字符两个字节的顺序写入输出流。
void writeDouble(double v)
// 将由八个字节组成的双精度值写入输出流。
void writeFloat(float v)
// 将由四个字节组成的单精度值写入输出流。
void writeInt(int v)
// 将由四个字节组成的整形值写入输出流。
void writeLong(long v)
// 将由八个字节组成的长整形值写入输出流。
void writeShort(int v)
// 将由四个字节组成的短整形值写入输出流。
void writeUTF(String s)
// 将两个字节的长度信息写入输出流，后面是字符串s中每个字符的修改后的UTF-8表示。
```
