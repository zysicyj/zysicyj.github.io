---
uuid: a7f6c670-5797-11ee-8d4d-618abb08a74a
title: 说一说springboot加载配置文件优先级
tags:
  - springboot
  - 加载配置文件
  - 优先级
  - 命令行参数
  - 操作系统环境变量
  - 命令行属性
  - jar包外部的配置文件
  - jar包内部的配置文件
  - jar包外部的profile配置文件
  - jar包内部的profile配置文件
categories: []
abbrlink: fed94248
date: 2023-09-20 17:25:36
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`

> 全网最细面试题手册，支持艾宾浩斯记忆法。这是一份最全面、最详细、最高质量的 java
面试题，不建议你死记硬背，只要每天复习一遍，有个大概印象就行了。 `https://store.amazingmemo.com/chapterDetail/1685324709017001`
    




---
Spring Boot加载配置文件的优先级是根据不同的位置和命名规则来确定的。下面按照优先级从高到低的顺序来介绍：

1. **命令行参数**：通过命令行参数指定的配置会覆盖其他配置。例如，使用`--spring.config.name`和`--spring.config.location`
   参数可以指定配置文件的名称和位置。

2. **操作系统环境变量**：Spring Boot会自动将操作系统环境变量中以`SPRING_`
   开头的变量转换为配置属性。例如，将`SPRING_APPLICATION_NAME`设置为`myapp`
   ，则可以在配置文件中使用`${spring.application.name}`来引用该值。

3. **命令行属性**：可以通过`-D`参数或者`--spring.config.name`和`--spring.config.location`参数来指定配置文件的名称和位置。

4. **jar包外部的application.properties或application.yml**：如果存在`config`文件夹，Spring
   Boot会加载该文件夹下的`application.properties`或`application.yml`文件。

5. **jar包内部的application.properties或application.yml**：如果jar包内部存在`application.properties`或`application.yml`
   文件，Spring Boot会加载该文件。

6. **jar包内部的application-{profile}.properties或application-{profile}.yml**：如果指定了激活的profile，Spring
   Boot会加载对应的`application-{profile}.properties`或`application-{profile}.yml`文件。

7. **jar包外部的application-{profile}.properties或application-{profile}.yml**：如果存在`config`文件夹，Spring
   Boot会加载该文件夹下的`application-{profile}.properties`或`application-{profile}.yml`文件。

8. **jar包外部的application.properties或application.yml**：如果存在`config`文件夹，Spring
   Boot会加载该文件夹下的`application.properties`或`application.yml`文件。

需要注意的是，Spring Boot会按照上述顺序加载配置文件，后面加载的配置会覆盖前面加载的配置。因此，如果存在多个配置文件，可以通过优先级来控制配置的加载顺序。

另外，Spring Boot还支持使用`@PropertySource`注解来加载自定义的配置文件，可以通过`value`
属性指定配置文件的路径。这种方式的优先级介于jar包内部和jar包外部的配置文件之间。

总结起来，Spring Boot加载配置文件的优先级从高到低依次为：命令行参数 > 操作系统环境变量 > 命令行属性 >
jar包外部的配置文件 > jar包内部的配置文件 > jar包外部的profile配置文件 > jar包内部的profile配置文件。

