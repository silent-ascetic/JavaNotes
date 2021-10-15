java当中默认声明的小数是double类型的；

 * double d=4.0

 * 如果声明：

 * float x = 4.0则会报错，需要如下写法：

 * float x = 4.0f或者float x = (float)4.0

 * 其中4.0f后面的f只是为了区别double，并不代表任何数字上的意义

 * 

 * float表示单精度浮点数在机内占4个字节，用32位二进制描述

 * double表示双精度浮点数在机内占8个字节，用64位二进制描述



 * 对编程人员来说，double 和 float 的区别是double精度高，有效数字16位，float精度7位。但double消耗内存是float的两倍，double的运算速度比float慢得多，java语言中数学函数名称double 和 float不同，不要写错，能用单精度时不要用双精度(以省内存，加快运算速度)。



float：

```java
float x = 3.56412f;  
float y = 5.13f;  
System.out.println(x+y);
```
 输出：8.69412


 *  在《Effective Java》这本书中也提到这个原则： float和double只能用来做科学计算或者是工程计算; 在商业计算中我们要用java.math.BigDecimal。

如下代码：

 

```java 
double z = 3.564;  
double a = 5.13;  
System.out.println(z+a);  
 输出：8.693999999999999
```


如果使用java.math.BigDecimal类进行计算：

```java 
/** 
 * 提供精确的加法运算。 
 * @param v1 被加数 
 * @param v2 加数 
 * @return 两个参数的和 
 */  
 public static double add(double v1,double v2)  
 {  
     BigDecimal b1 = new BigDecimal(Double.toString(v1));  
     BigDecimal b2 = new BigDecimal(Double.toString(v2));  
     return b1.add(b2).doubleValue();  
 }  
```
 输出：8.694


由此引出减法的计算：

```java 
/** 
 * 提供精确的减法运算。 
 * @param v1 被减数 
 * @param v2 减数 
 * @return 两个参数的差 
 */  
 public static double sub(double v1,double v2){  
     BigDecimal b1 = new BigDecimal(Double.toString(v1));  
     BigDecimal b2 = new BigDecimal(Double.toString(v2));  
     return b1.subtract(b2).doubleValue();  
 }  
```

乘法的计算：

```java
/** 
 * 提供精确的乘法运算。 
 * @param v1 被乘数 
 * @param v2 乘数 
 * @return 两个参数的积 
 */  
 public static double mul(double v1,double v2) {  
     BigDecimal b1 = new BigDecimal(Double.toString(v1));  
     BigDecimal b2 = new BigDecimal(Double.toString(v2));  
     return b1.multiply(b2).doubleValue();  
 }  
```

 除法的计算：

```java
/** 
 * 提供（相对）精确的除法运算，当发生除不尽的情况时，精确到 
 * 小数点以后10位，以后的数字四舍五入。 
 * @param v1 被除数 
 * @param v2 除数 
 * @return 两个参数的商 
 */  
 public static double div(double v1,double v2) {  
     return div(v1,v2,10);  
 }  
 /** 
 * 提供（相对）精确的除法运算。当发生除不尽的情况时，由scale参数指 
 * 定精度，以后的数字四舍五入。 
 * @param v1 被除数 
 * @param v2 除数 
 * @param scale 表示表示需要精确到小数点以后几位。 
 * @return 两个参数的商 
 */  
 public static double div(double v1,double v2,int scale){  
     if(scale<0){  
         throw new IllegalArgumentException("The scale must be a positive integer or zero");  
     }  
     BigDecimal b1 = new BigDecimal(Double.toString(v1));  
     BigDecimal b2 = new BigDecimal(Double.toString(v2));  
     return b1.divide(b2,scale,BigDecimal.ROUND_HALF_UP).doubleValue();  
 }  
```


提供精确的小数位四舍五入处理：

```java
/** 
 * 提供精确的小数位四舍五入处理。 
 * @param v 需要四舍五入的数字 
 * @param scale 小数点后保留几位 
 * @return 四舍五入后的结果 
 */  
 public static double round(double v,int scale) {  
     if(scale<0){  
         throw new IllegalArgumentException("The scale must be a positive integer or zero");  
     }  
     BigDecimal b = new BigDecimal(Double.toString(v));  
     BigDecimal one = new BigDecimal("1");  
     return b.divide(one,scale,BigDecimal.ROUND_HALF_UP).doubleValue();  
 }  
```
