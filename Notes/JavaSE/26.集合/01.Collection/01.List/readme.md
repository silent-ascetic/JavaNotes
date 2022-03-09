# List

List是Collection的子接口，作为集合的一个分支


## 特点

1. 无序：集合中的元素无顺序
2. 元素下标从零开始

## 常用方法

```text
boolean add(E e); //向尾部添加元素

void add(int index, E e); //向指定位置插入元素

boolean addAll(Collection<? extends E> c); //将参数集合中的元素添加到集合结尾，插入顺序为迭代器迭代顺序

E get(int index); //返回集合中参数位置的元素

ListIterator<E> listIterator(); //返回调用集合的迭代器

int indexOf(Object obj); //返回参数在集合中第一次出现的位置，若无此参数返回-1

int LastIndexOf(Object obj); //返回参数在集合中最后出现的位置，无则返回-1

E remove(int index); //删除集合中指定位置元素并返回该元素

boolean remove(Object obj); //删除集合中指定元素，若有多个则删除第一个

void clear(); //清空集合

boolean removeAll(Collection<?> c); //删除集合中参数集合包含的元素

E set(int index, E element); //用指定元素替代集合中指定位置元素并返回改元素
```



