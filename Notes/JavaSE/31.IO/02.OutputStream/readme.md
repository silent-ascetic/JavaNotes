# OutputStream

> 字节输出流

```java
package java.io.OutputStream;

public abstract class OutputStream extends Object implements Closeable, Flushable {}
```

## 方法

```text
void close()
// 关闭此输出流并释放与此流关联的所有系统资源。
void flush()
// 刷新此输出流，并强制写出所有缓冲的输出字节。
void write(byte[] b)
// 将指定字节数组中的字节写入此输出流。
void write(byte[] b, int off, int len)
// 从偏移量off开始，将指定字节数组中的len个字节写入此输出流。
abstract void write(int b)
// 将字节写入输出流
```