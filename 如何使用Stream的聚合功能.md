---
uuid: 78264b60-4de1-11ee-8cfe-478cc7650eda
title: 如何使用Stream的聚合功能
tags: []
categories: []
abbrlink: e8e4863e
date: 2023-09-08 08:48:47
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`

> 全网最细面试题手册，支持艾宾浩斯记忆法。这是一份最全面、最详细、最高质量的 java
面试题，不建议你死记硬背，只要每天复习一遍，有个大概印象就行了。 `https://store.amazingmemo.com/chapterDetail/1685324709017001`
    




---

1. 求和（Sum）：

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int sum = numbers.stream().mapToInt(Integer::intValue).sum();
System.out.println("Sum: " + sum);
```

2. 求平均值（Average）：

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
double average = numbers.stream().mapToInt(Integer::intValue).average().orElse(0.0);
System.out.println("Average: " + average);
```

3. 最大值（Max）：

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int max = numbers.stream().mapToInt(Integer::intValue).max().orElse(0);
System.out.println("Max: " + max);
```

4. 最小值（Min）：

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int min = numbers.stream().mapToInt(Integer::intValue).min().orElse(0);
System.out.println("Min: " + min);
```

5. 计数（Count）：可以使用`count()`方法来计算Stream中元素的个数。

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
long count = numbers.stream().count();
System.out.println("Count: " + count);
```

6. 连接字符串（Joining）：可以使用`collect()`方法结合`Collectors.joining()`来将Stream中的元素连接成一个字符串。

``` java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
String joinedNames = names.stream().collect(Collectors.joining(", "));
System.out.println("Joined Names: " + joinedNames);
```

7. 分组（Grouping）：可以使用`collect()`方法结合`Collectors.groupingBy()`来根据某个属性对Stream中的元素进行分组。

``` java
List<Person> people = Arrays.asList(
    new Person("Alice", 25),
    new Person("Bob", 30),
    new Person("Charlie", 25)
);
Map<Integer, List<Person>> peopleByAge = people.stream().collect(Collectors.groupingBy(Person::getAge));
System.out.println("People grouped by age: " + peopleByAge);
```

8. 求和（Summarizing）：可以使用`collect()`方法结合`Collectors.summarizingInt()`等方法来获取元素的汇总信息，如求和、平均值、最大值、最小值等。

``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
IntSummaryStatistics stats = numbers.stream().collect(Collectors.summarizingInt(Integer::intValue));
System.out.println("Sum: " + stats.getSum());
System.out.println("Average: " + stats.getAverage());
System.out.println("Max: " + stats.getMax());
System.out.println("Min: " + stats.getMin());
```


