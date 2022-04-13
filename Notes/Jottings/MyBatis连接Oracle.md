# MyBatis连接Oracle遇到的问题

## 类型转换异常

**报错信息：**

ERROR 18872 --- [nio-8081-exec-1] o.a.c.c.C.[.[.[/].[dispatcherServlet]    : Servlet.service() for servlet [dispatcherServlet] in context with path [] threw exception [Request processing failed; nested exception is org.springframework.jdbc.UncategorizedSQLException: Error attempting to get column 'ID' from result set.  Cause: java.sql.SQLException: 不支持的字符集 (在类路径中添加 orai18n.jar): ZHS16GBK; uncategorized SQLException; SQL state [99999]; error code [17056]; 不支持的字符集 (在类路径中添加 orai18n.jar): ZHS16GBK; nested exception is java.sql.SQLException: 不支持的字符集 (在类路径中添加 orai18n.jar): ZHS16GBK] with root cause

java.sql.SQLException: 不支持的字符集 (在类路径中添加 orai18n.jar): ZHS16GBK

**解决方案：**

项目缺少orai18n依赖，在maven中加入orai18n依赖即可。

**注：**

maven依赖搜索网站：
[https://mvnrepository.com](https://mvnrepository.com/)


## 查出来的数据有的值为null

查出来的数据转换成对应Java对象后，对象中有的属性值为null

```xml
<select id="selectByName"  resultType="com.example.domain.User">
    select * from user where username = #{name}
</select>
```

**解决方法**

为User类创建一个resultMap
```xml
<resultMap id="BaseResultMap" type="com.example.domain.User">
    <id property="id" column="ID" jdbcType="DECIMAL"/>
    <result property="name" column="NAME" jdbcType="VARCHAR"/>
    <result property="password" column="PASSWORD" jdbcType="VARCHAR"/>
    <result property="sex" column="SEX" jdbcType="VARCHAR"/>
    <result property="birthday" column="BIRTHDAY" jdbcType="TIMESTAMP"/>
    <result property="email" column="EMAIL" jdbcType="VARCHAR"/>
</resultMap>

<select id="selectByName"  resultMap="BaseResultMap">
    select * from user where username = #{name}
</select>
```
