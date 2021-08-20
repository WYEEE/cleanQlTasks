# 清理青龙面板重复任务



**警告：本程序仅通过任务名称判断是否重复，不排除误删的可能**

## 使用本仓库前提

安装了青龙面板，且能通过`/ql/config/auth.json`路径访问到用户名，密码，和token



## 使用方法：

1、将仓库的clone下来，将其放在/ql/scripts下，目录结构如下

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820220115801.png" alt="image-20210820220115801" style="zoom: 50%;" />

2、青龙面板中如下添加任务

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820224311591.png" alt="image-20210820224311591" style="zoom:50%;" />

3、可以直接运行一下试试

原先一共有：

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820221200972.png" alt="image-20210820221200972" style="zoom:50%;" />

点击运行：

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820221125603.png" alt="image-20210820221125603" style="zoom:50%;" />

查看日志：

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820221341094.png" alt="image-20210820221341094" style="zoom:50%;" />

回去再看一下：

<img src="https://gitee.com/AndrewYu/PicGo/raw/master/img/image-20210820221407319.png" alt="image-20210820221407319" style="zoom:50%;" />



## 代码运行流程：

1、读取/ql/config/auth.json中的token，向localhost:5700发起请求，获得task列表

2、对比task的名称，仅保留不重复的任务

3、向对应api发出delete请求，删除重复的任务



# 鸣谢：

本仓库的推送功能来自curtinlv@github：https://github.com/curtinlv/JD-Script/blob/main/sendNotify.py，在他的代码的基础上，我修改了server酱推送的一个bug(其他推送方式我没测试)





