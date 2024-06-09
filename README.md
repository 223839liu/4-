# 第一二节课

## GitHub


### 关键字查询
xx(python) awesome:查询该标签下的xx(python)项目
xx(python) tutorial:查询xx(python)资料，书籍，文档
xx(socket) sample:查询对应技术（socket）的代码样本


### github三要素
**Repository 仓库:**
  仓库是github项目管理存储基本单位
一个仓库中存储一个项目，一个用户可以拥有多个仓
库，一般仓库分为public， private
**Commit 提交:**
  程序员在整个开发周期， 有大量的对代码资源的选代
和修改，都可以通过commit的方式进行记录,便于程
序员回溯代码,即使这些代码被删除
提交便于使用者观察整个工程的开发流程以及设计流
程
**Branch 分支:**
  在仓库中可以包含多个分支，分支才是代码文件的第
一存储单位，默认的仓库主分支为master/main
\*不仅可以管理代码存储， 便于多人协作开发
[![2.png](https://i.postimg.cc/ZnKj7mf0/2.png)](https://postimg.cc/Fd8jzMXQ)

### 仓库内容
Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等
issues，使用时遇到的bug 或进行提交，等待反馈
README，使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等
LICENSE 许可证
  GPL2.0，3.0.Apahce 2.0，Mit， 这些许可证，给使用者最大使用权限以及最少的限制

### git软件，分布式版本控制系统
[![3.png](https://i.postimg.cc/fyr789tg/3.png)](https://postimg.cc/fSY0Lkvx)

### 设备认证
**1.如何让网站的账户与设备绑定， 后续完成代码的管理， 上传下载**
```bash
   git init //创建本地仓库   //*后续对仓库的操作，都要在仓库位置(master)
   git config --list //查看git的配置文件
   git config --global useremail "邮箱
   git config --global username“用户名    SSH 远程访问
   ssh-keygen -t rsa -C “注册邮箱” //创建本地密文
*去对应的目录查找密文文件
   rsa.pub 复制密文, 粘贴 settings -> SSH key and GPG > new ssh key - >粘贴
   ssh -T git@github.com// 测试关联是否成功
```

**2.为目标仓库起别名， 定位目标仓库， 后续上传**
```bash
   git remote add orgin “ssh地址”//为ssh仓库地址创建别名为origin
   git remote remove orgin //删除origin别名
   git remote add orgin “ssh地址”//为ssh仓地址创建别名为origin
```

### 本地设备与云端仓库的交互逻辑
[![4.png](https://i.postimg.cc/Sx0CjqW8/4.png)](https://postimg.cc/fJKJgGqT)


### 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致，本地内容无法再次提交
先拉取 git puI 云端内容 与本地内容合并或操作，而后再次推即可
```bash
   git pull --rebase origin master
   git rebase --skip“忽略本地内容 保留云端内容
   git rebase --abort"忽略本地内容 保留云端内容
   git rebase --continue“忽略本地内容 保留云端内容
```

### 下载开源代码
```bash
   git clone"https仓库地址"//下载开源项目code资源
```

### 分支Branch
关于分支的相关命令， 创建分支、 选择分支、 合并分支等等

### MarkDown语言
github可编写readme，文本修饰语言


# 第三节课


## 标题修饰符

# 标题修饰符（一级标题）
## （二级标题）
### (三级标题)
#### （四级标题）


## 正文内容

输入正文内容，但如果需要换行，用\<br\>标签


## 修饰正文


*一段文本*<br>
**一段文本**


***一段文本***<br>
~~一段文本~~

一段文本的`关键字`


## 分割线用\-\-\-或\~\~\~表示

---



## 引用用\>表示
>引用
>>引用
>>>引用
>>>>引用

## 列表修饰符
### 无序列表\*
* 二次元游戏
  * 原神
    * 神里凌华
* 大逃杀
  * PUBG
  * 黎明杀机
### 有序列表 1.
1. 物理学
   1. 经典物理学
   2. 量子物理学
### 混用列表
1. 人
   * 四肢
    1. 手
---

### 表格
人名|技能|排行
--|:--:|--:|
蜘蛛侠|失败的man|1
海王|钓鱼|2

### 插入代码片段
```c
   #include<stdio.h>
   int main()
   {
      printf("holle world\n");
      return 0;
   }
```

```cpp
   #include<iostream>
   uisng namespace std;
   int main()
   {
   cout<<"hello world"<<endl;
   return 0;
   }
```
```bash
   ls -a
   pwd 
   cd .
```

### 超链接
[github](https://github.com"点击访问")


### 插入图片
[![1.png](https://i.postimg.cc/bJfBRKc2/1.png)](https://postimg.cc/jWvcx3js)
