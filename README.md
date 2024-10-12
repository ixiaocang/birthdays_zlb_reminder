# birthdays_reminder
免费的邮件成员生日提醒。适应于行政部门，社团，好友，生日时当天提醒自己。作者INKCOO(ixiaocang/Hitori/小东/修兮求索/radish)
## 项目简介
这是一个用于生日提醒的 Python 程序，它可以通过读取生日列表，在生日当天自动发送邮件提醒。支持公历和农历生日提醒，适用于使用 QQ 邮箱发送邮件。生日提醒邮件不仅会发送给生日人，还会发送一份提醒邮件给管理员。项目为我想记得给校心助会成员生日祝福初衷设计。
作者INKCOO(ixiaocang/Hitori/小东/修兮求索/radish)目前是本科日专生，计算机超级菜鸟一个，利用AI创建的程序，有问题或建议请邮ixiaocang@foxmail.com。请轻喷。
### 功能
- **生日提醒**：支持公历和农历生日提醒，自动判断是否为当天生日。
- **邮件发送**：在生日当天，自动发送邮件提醒管理员。
- **日志记录**：记录程序启动时间、结束时间和运行时长到日志文件中。
- **可配置性**：通过环境变量配置邮箱账号、密码和管理员邮箱，确保敏感信息的私密性。

### 通过github免费使用方法

**1.克隆到自己的仓库**

**2.配置生日列表**：
在项目根目录下 `birthdays.txt` 文件，按照如下格式添加成员的生日信息：
姓名-月-日-公历或农历类型
例如：
张三-10-12-a
李四-08-15-b
#a代表公历（阳历），b代表农历（阴历）

**3.配置邮件客户端**
登录到你的QQ邮箱账户。
在右上角点击“设置”图标（齿轮形状）。
选择“账户”选项。
找到“SMTP服务”部分，并点击“开启”按钮。
你需要设置一个授权码，这个授权码是你程序中的smtp_password。点击“生成授权码”，系统会生成一个16位的授权码，记下来。
**4.储存环境变量（邮箱信息私密化）**
进入你的GitHub仓库：
打开“Settings”（设置）：
在页面右上角，点击“Settings”标签。

找到“Secrets and variables”（机密和变量）：
在左侧菜单中，找到“Secrets and variables”选项，点击“Actions”。

添加新的Secret：
点击“New repository secret”按钮。

在“Name”字段中输入一个名称，例如 SMTP_USER 或 SMTP_PASSWORD 或ADMIN_EMAIL。
在“Value”字段中输入你的邮箱和授权码。
点击“Add secret”按钮保存。
依次添加完SMTP_USER,SMTP_PASSWORD,ADMIN_EMAIL
## 到此你的项目就配置好了，在.github/workflows/birthday_reminder.yml工作流中可以手动运行测试
**也可以在工作流中修改程序运行时间**
当前为明天北京时间上午8:05运行，因为github自动任务有延迟，实际运行时间会推迟
不建议将时间提前，因为受github时区影响，可能会产生一点问题
部署到本地服务器的话只要，可以修改时间。只要复制birthday_reminder.py文件和birthdays.txt，通过计划任务运行就好了。

## CC BY-NC-ND 4.0 许可证

本项目采用 [知识共享署名-非商业性使用-禁止演绎 4.0 国际许可协议](https://creativecommons.org/licenses/by-nc-nd/4.0/) 进行许可。

### 你可以：
- **查看**并**使用**本项目的代码，用于非商业用途。

### 你不可以：
- **修改**、**派生**或**再分发**修改后的版本。
- 将本项目用于**商业用途**。

如需获得其他用途的许可，请联系作者ixiaocang@foxmail.com。
