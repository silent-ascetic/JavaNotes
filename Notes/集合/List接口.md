# List<E>

## 特点

1. 无序，集合中的元素无顺序
2. 元素下标从零开始

## 常用方法

```java
boolean add(E e); //向尾部添加元素
void add(int index, E e); //向指定位置插入元素
boolean addAll(Collection<? extends E> c); //将参数集合中的元素添加到集合结尾，插入顺序为迭代器迭代顺序
E get(int index); //返回集合中参数位置的元素
ListIterator<E> listIterator(); //返回调用集合的迭代器

```

## ListIterator

专门用来遍历List集合的类



