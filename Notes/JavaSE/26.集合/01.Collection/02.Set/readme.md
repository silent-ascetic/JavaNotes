# Set

> ```java
> public interface Set<E> extends Collection<E>{}
> ```

一个不包含重复元素的collection。更确切地讲，set 不包含满足e1.equals(e2)的元素对e1 和e2，并且最多包含一个null 元素。

## 方法

```text
boolean add(E e)
// 如果set 中尚未存在指定的元素，则添加此元素（可选操作）。
boolean addAll(Collection<? extends E> c)
// 如果set 中没有指定collection 中的所有元素，则将其添加到此set 中（可选操作）。
void clear()
// 移除此set 中的所有元素（可选操作）。
boolean contains(Object o)
// 如果set 包含指定的元素，则返回true。
boolean containsAll(Collection<?> c)
// 如果此set 包含指定collection 的所有元素，则返回true。
boolean equals(Object o)
// 比较指定对象与此set 的相等性。
int hashCode()
// 返回set 的哈希码值。
boolean isEmpty()
// 如果set 不包含元素，则返回true。
Iterator<E> iterator()
// 返回在此set 中的元素上进行迭代的迭代器。
boolean remove(Object o)
// 如果set 中存在指定的元素，则将其移除（可选操作）。
boolean removeAll(Collection<?> c)
// 移除set 中那些包含在指定collection 中的元素（可选操作）。
boolean retainAll(Collection<?> c)
// 仅保留set 中那些包含在指定collection中的元素（可选操作）。
int size()
// 返回set 中的元素数（其容量）。
Object[] toArray()
// 返回一个包含set 中所有元素的数组。
<T> T[] toArray(T[] a)
// 返回一个包含此set 中所有元素的数组；返回数组的运行时类型是指定数组的类型。
```
