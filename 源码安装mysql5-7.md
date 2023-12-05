---
uuid: a74dff2e-4416-11ee-9ac2-67d3233bf96f
title: 源码安装mysql5.7
tags:
  - mysql
  - 源码
  - 安装
abbrlink: 3f760569
date: 2023-08-19 17:25:01
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`

# 通过 RPM 包安装 MySQL

1. **下载 MySQL RPM 包：** 首先，您需要从 MySQL 官方网站（https://dev.mysql.com/downloads/mysql/）下载适用于您的操作系统版本和架构的
   MySQL RPM 包。选择与您的操作系统和系统架构相对应的版本。

2. **安装 RPM 包：** 下载完成后，您可以使用 `rpm` 命令安装 MySQL RPM 包。假设您下载的 RPM 包名为 `mysql.rpm`，您可以使用以下命令进行安装：
   ``` bash
   sudo rpm -ivh mysql.rpm
   ```

3. **启动 MySQL 服务：** 安装完成后，您可以使用以下命令启动 MySQL 服务：
   ``` bash
   sudo systemctl start mysql
   ```

4. **设置开机启动：** 若要确保系统重启后 MySQL 服务能够自动启动，可以使用以下命令启用开机自启动：
   ``` bash
   sudo systemctl enable mysql
   ```

5. **设置 MySQL 根密码：** 安装 MySQL 后，需要设置 MySQL 根用户的密码。可以使用以下命令进行设置：
   ``` bash
   sudo mysql_secure_installation
   ```

6. **访问 MySQL：** 安装和配置完成后，您可以使用以下命令登录到 MySQL 数据库：
   ``` bash
   mysql -u root -p
   ```

# 给root用户取消IP配置

在 MySQL 数据库中，有时默认会限制 root 用户只能通过 localhost（127.0.0.1）连接，以提高安全性。如果您希望允许 root 用户从其他主机连接到
MySQL，您可以按照以下步骤取消 root 用户的 IP 限制：

1. **编辑 MySQL 配置文件：** 打开 MySQL 的配置文件，通常是 `/etc/my.cnf` 或 `/etc/mysql/my.cnf`
   ，使用您喜欢的文本编辑器（例如 `nano` 或 `vim`）：
   ``` bash
   sudo nano /etc/my.cnf
   ```

2. **在 `[mysqld]` 段添加 `skip-networking` 行：** 在配置文件中找到 `[mysqld]`
   段，在该段中添加以下行以禁用 `skip-networking` 选项，确保其处于注释状态（行前面有 `#`）：
   ```
   # skip-networking
   ```

3. **重启 MySQL 服务：** 保存配置文件后，重启 MySQL 服务以应用更改：
   ``` bash
   sudo systemctl restart mysql
   ```

4. **登录 MySQL 并更新 root 用户权限：** 现在您可以登录到 MySQL 数据库，并为 root 用户设置允许从其他主机连接的权限。打开终端，输入以下命令登录到
   MySQL：
   ``` bash
   mysql -u root -p
   ```

5. **更新 root 用户的主机设置：** 在 MySQL 命令行中，使用以下 SQL 命令更新 root 用户的主机设置，允许从任何主机连接：
   ``` sql
   GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'your_password' WITH GRANT OPTION;
   ```
   请将 `'your_password'` 替换为您希望设置的 root 用户密码。

6. **刷新权限：** 更新了权限设置后，执行以下 SQL 命令以刷新 MySQL 的权限：
   ``` sql
   FLUSH PRIVILEGES;
   ```

7. **退出 MySQL 命令行：** 输入以下命令退出 MySQL 命令行：
   ``` shell
   EXIT;
   ```

# 详细解读mysql5.7的配置文件

��读mysql5.7的配置文件


