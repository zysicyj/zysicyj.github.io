---
uuid: 16bbf4a0-48d3-11ee-ab49-893c6917aa08
title: SpringBoot的传播机制详解
tags:
  - Spring Boot
  - 传播机制
  - 事务管理
  - 技术文章
  - 后端技术
  - 系列文章
  - 面试题精讲
abbrlink: "29182850"
date: 2023-09-01 22:23:15
---


[首发博客地址](https://blog.zysicyj.top/ "首发博客地址")

[系列文章地址](https://blog.zysicyj.top/categories/技术文章/后端技术/系列文章/面试题精讲/ "系列文章地址")


---

Spring Boot 是基于 Spring 框架的快速开发框架，提供了许多便捷的特性和机制来简化开发过程。在 Spring Boot
中，事务的传播机制是通过@Transactional 注解来实现的。

@Transactional 注解可以用于方法、类或接口上，用于标识方法或类中的所有方法需要进行事务管理。通过设置@Transactional 注解的
propagation 属性，可以指定事务的传播行为。

事务的传播行为分为以下几种：

1. REQUIRED：表示当前方法必须在一个事务内运行。如果当前已经存在事务，则加入该事务；如果当前不存在事务，则创建一个新的事务。

2. SUPPORTS：表示当前方法支持事务。如果当前存在事务，则加入该事务；如果当前不存在事务，则以非事务方式运行。

3. MANDATORY：表示当前方法必须在一个事务内运行。如果当前不存在事务，则抛出异常。

4. REQUIRES_NEW：表示当前方法必须在一个新的事务内运行。如果当前存在事务，则挂起该事务并创建一个新的事务。

5. NOT_SUPPORTED：表示当前方法不支持事务。如果当前存在事务，则挂起该事务。

6. NEVER：表示当前方法不支持事务。如果当前存在事务，则抛出异常。

7. NESTED：表示当前方法必须在一个嵌套事务内运行。如果当前存在事务，则在嵌套事务内运行；如果当前不存在事务，则创建一个新的事务。

下面是一个使用 Spring Boot 传播机制的示例：

``` java
@Service
@Transactional(propagation = Propagation.REQUIRED)
public class UserService {

    @Autowired
    private UserRepository userRepository;

    public void createUser(User user) {
        // 保存用户信息
        userRepository.save(user);

        // 调用其他方法，如果其他方法也有@Transactional注解，则会参与到当前事务中
        updateUserStatus(user.getId());
    }

    @Transactional(propagation = Propagation.REQUIRED)
    public void updateUserStatus(Long userId) {
        // 更新用户状态
        userRepository.updateStatus(userId);
    }
}
```

在上面的示例中，UserService 类的 createUser 方法使用了@Transactional 注解，并设置了传播行为为
REQUIRED，表示该方法必须在一个事务内运行。在该方法中，先保存用户信息到数据库，然后调用了 updateUserStatus 方法。由于
updateUserStatus 方法也使用了@Transactional 注解，并且传播行为也为 REQUIRED，所以它会参与到当前事务中，保证了两个方法的操作在同一个事务内执行。

通过使用@Transactional 注解，我们可以方便地控制事务的传播行为，实现对数据库操作的事务管理。


