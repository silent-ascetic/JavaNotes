# Map

所在包：java.util

Interface Map<K,V>

参数类型
K - 键的类型
V - 映射值的类型

所有已知子接口:
`Bindings ， ConcurrentMap <K，V>， ConcurrentNavigableMap <K，V>， LogicalMessageContext ， MessageContext ， NavigableMap <K，V>， SOAPMessageContext ， SortedMap <K，V>`

所有已知实现类：
`AbstractMap ， Attributes ， AuthProvider ，ConcurrentHashMap ， ConcurrentSkipListMap ， EnumMap ，HashMap ， Hashtable ， IdentityHashMap ， LinkedHashMap ， PrinterStateReasons ， Properties ， Provider ， RenderingHints ， SimpleBindings ， TabularDataSupport ， TreeMap ， UIDefaults ， WeakHashMap`

这个接口取代了Dictionary类，后者是一个完全抽象的类而不是接口。

**特点：**
- 无序
- 键不可重复
- 值可重复

## 常用方法

```java
interface Map<K, V> {
    void	clear();
// 删除所有的映射（可选操作）。

    boolean	containsKey(Object key);
// 如果此映射包含指定键的映射，则返回 true 。

    boolean	containsValue(Object value);
// 如果此map将一个或多个键映射到指定的值，则返回 true 。

    Set<Map.Entry<K,V>>	entrySet();
// 返回此map中包含的映射的Set视图。

    boolean	equals(Object o);
// 将指定的对象与此映射进行比较以获得相等性。

    V	get(Object key);
// 返回到指定键所映射的值,如果此映射包含该键的映射,或 null。

    default V	getOrDefault(Object key, V defaultValue);
// 返回到指定键所映射的值，如果此映射包含该键的映射,或 defaultValue。

    int	hashCode();
// 返回此map的哈希码值。

    boolean	isEmpty();
// 如果此map不包含键值映射，则返回 true 。

    Set<K>	keySet();
// 返回此map中包含的键的Set视图。

    default V	merge(K key, V value, BiFunction<? super V,? super V,? extends V> remappingFunction);
// 如果指定的键尚未与值相关联或与null相关联，则将其与给定的非空值相关联。

    V	put(K key, V value);
// 将指定的值与该映射中的指定键相关联（可选操作）。

    void	putAll(Map<? extends K,? extends V> m);
// 将指定map的所有映射复制到此映射（可选操作）。

    default V	putIfAbsent(K key, V value);
// 如果指定的键尚未与某个值相关联（或映射到 null ）将其与给定值相关联并返回 null ，否则返回当前值。

    V	remove(Object key);
// 如果存在，从该map中删除一个键的映射。

    default boolean	remove(Object key, Object value);
// 仅当指定的键映射到指定的值时删除该条目。

    default V	replace(K key, V value);
// 只有当目标映射到某个值时，才能替换指定键的条目。

    default boolean	replace(K key, V oldValue, V newValue);
// 仅当当前映射到指定的值时，才能替换指定键的条目。

    default void	replaceAll(BiFunction<? super K,? super V,? extends V> function);
// 将每个条目的值替换为对该条目调用给定函数的结果，直到所有条目都被处理或该函数抛出异常。

    int	size();
// 返回此map中键值映射的数量。

    Collection<V>	values();
// 返回此map中包含的值的Collection视图。
}

```

