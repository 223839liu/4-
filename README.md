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

###进程
1.单任务操作系统(单进程模式，一个时刻只能执行一个任务)
2.如果要在古早时期电脑中执行多个软件，需要将当前占用的交换出来存储在软盘中，而后执行新任务
3.需要让电脑中多个执行单位合理共享使用硬件资源，这也是多任务操作系统的前提

PROCESS进程
操作系统默认的执行单元， 可以使用cpu 内存磁盘等等系统设备，完成特定任务，进程是最经典的调度单


[![QQ-20240716095949.png](https://i.postimg.cc/13NcRP5g/QQ-20240716095949.png)](https://postimg.cc/xXnbgwmY)
[![QQ-20240716133857.png](https://i.postimg.cc/gc13SjWx/QQ-20240716133857.png)](https://postimg.cc/rzCdz8zT)

Linux进程状态
就绪态、运行态、睡眠态、挂起态、终止态、僵尸态、孤儿态
Linux进程开发，进程源语
操作系统提供的一系列API函数接口，开发者可以使用完成进程功能开发任务
```linux
   pid_t gork(void)//进程创建，调用一次创建一个进程
```

```c
   #include<stdio.h>
   #include<unistd.h>
   #include<stdlib.h>
   #include<string.h>
   #include<sys/types.h
   #include<sys/stat.h>
   #include<sys/fcntl.h>
   #include<pthread.h>
   #include<signal.h>
//父进程从代码段的起始执到末尾，子进程被fork()创建，从fork之后执行到未尾
int main(void){
pid_t pid;
pid = fork() :
//fork创建成功,父进程中返回子进程的pid 33365 33366
//在子进程中返回0,如果创建失败返回-1
//pid == 33366
if(pid > 0){
//父进程工作区
printf("parent Runing ...\n");
while(1);
}
//pid == 0
else if(pid ==0){
//子进程工作区
printf("child Runing....\n");
while(i);
}else{
perror("fork call failed") ;
exit(0);
}
return 0;
}
```
[![9735.png](https://i.postimg.cc/Qtbng7PK/9735.png)](https://postimg.cc/Kk1Nx1mm)
不允许子进程踏出自己的工作区（else if代码快），子进程执行完自己的代码块通过exit（）结束进程
```c
   #include<stdio.h>
   #include<unistd.h>
   #include<stdlib.h>
   #include<string.h>
   int main(void){
   pid_t pid;
   int i;
   for(i=0;i<5;i++){
   pid =fork():
   if(pid == 0)
   break;
   }
   if(pid > 0){
   printf("parent pid %d\n",getpid());
   while(1)
   sleep(1);
   }else if(pid == 0){
   printf("child pid %d\n",getpid(),i);
   while(1)
   sleep(1);
   }else(
   perror("fork call failed");
   exit(0);
   }
   return 0;
   }
```
父子进程的继承与拷贝
[![1.png](https://i.postimg.cc/cHnf0G7x/1.png)](https://postimg.cc/WFsdwKfC)
execl(const char \* psth,argv[0],argv[1],NULL)//进程重载最后一个参数一定要传null，表示命令参数传递完毕，不写函数失败
[![2.png](https://i.postimg.cc/cHwtPMZ6/2.png)](https://postimg.cc/1nRzqF8Z)
```c
   #include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<sys/fcntl.h>
#include<pthread.h>
#include<signal.h>
int main(void)
{
//重载ls -l
pid_t pid;
pid=fork();
if(pid>0)
{
printf("Parent pid=%d\n",getpid());
while(1);
sleep(1);
}
else if(pid==0)
{
printf("Child pid=%d\n",getpid());
//execl("/bin/ls","ls","-l",NULL);
//重载浏览器
execl("/user/bin/firefox","firefox","www.baidu.com",NULL);
printf("execl success\n");
exit(0);
}
else
{
perror("fork failed");
exit(0);
}
}
```

zombie process 僵尸进程(zpid=wait(int * status)//进程回收，调用一次只回收一个僵尸，如果有多个僵尸进程，需要循环调用wait)
[![3.png](https://i.postimg.cc/gkSjSBRN/3.png)](https://postimg.cc/2VWC3G0Z)
```c
   #include<stdio .h>
#include<unistd.h>
#include<stdlib.h>
#include<string.h>
int main(void){
pid_t pid;
pid = fork();
if(pid >0){
printf("Parent pid %d Runing\n",getpid()) ;
while(1)
sleep(1);
}else if(pid == 0){
printf("Child pid %d Runingn",getpid());
sleep(5);
exit(0);
}else{
perror("fork call failed") ;
exit(0);
}
return 0;
}
#include<stdio .h>
#include<unistd.h>
#include<stdlib.h>
#include<string.h>
#include<sys/wait.h>
int main(void){
pid_t pid;
pid = fork();
if(pid >0){
printf("Parent pid %d Runing\n",getpid()) ;
zpid=wait(NULL);
printf("Parent wait success ,zpid %d\n",zpid);
while(1)
sleep(1);
}else if(pid == 0){
printf("Child pid %d Runingn",getpid());
sleep(5);
exit(0);
}else{
perror("fork call failed") ;
exit(0);
}
return 0;
}
```
wait函数，阻塞回收子进程（僵尸进程），主动回收方案，阻塞回收会影响父进程任务的执行，在等待过程中无法进行其他操作
[![4.png](https://i.postimg.cc/h47qWyH2/4.png)](https://postimg.cc/4nZ0p54c)
```c
#include<stdio .h>
#include<unistd.h>
#include<stdlib.h>
#include<string.h>
#include<sys/wait.h>
int main(void){
pid_t pid;
pid = fork();
if(pid >0){
printf("Parent pid %d Runing\n",getpid()) ;
while((zpid=waitpid(-1,NULL,WNOHANG))!=-1)
{
if(zpid==0)
{
printf("Parent 执行自身任务一次\n");
usleep(200000);
}
else if(zpid>0)
{
printf("回收成功，僵尸进程pid %d\n",zpid);
break;
}
}
while(1)
sleep(1);
}else if(pid == 0){
printf("Child pid %d Runingn",getpid());
sleep(5);
exit(0);
}else{
perror("fork call failed") ;
exit(0);
}
return 0;
}
```
[![5.png](https://i.postimg.cc/LsrNzTNs/5.png)](https://postimg.cc/SXf64W00)
```c
#include<stdio .h>
#include<unistd.h>
#include<stdlib.h>
#include<string.h>
#include<sys/wait.h>
#include<sys/types.h>
#include<sys/fcntl.h>
#include<pthread.h>
#include<signal.h>
#include<sys/stat.h>
int main(void)
{
pid_t pid;
int i;
for(i=0;i<2;i++)
{
pid=fork();
if(pid===0)
break;
}
if(pid>0)
{
printf("parent pid %d\n,waiting\n",getpid());
pid_t zpid;
int  status;
while((zpid==waitpid(-1,&status,WNOHANG))!=-1)
{
if(zpid==0)
{
//EAGAIN
}
else if(zpid>0)
{//验尸
if(WIFEXITED(status))
{//正常退出
printf("Zombie process %d,政策退出，退出码或返回值\n",zpid,WEXITSTATUS(status));
}
if(WIFSIGNALED(status))//异常退出
{
printf("Zombie process %d ,异常退出，信号编号 %d\n",zpid,WTERMSIG(status));
}
}
}
else if(pid==0)
{
if(i==0)
{
printf("child %d pid %d\n,runing..\n",i,getpid());
sleep(5);
printf("child %d pid %d\n,exiting..\n",i,getpid());
exit(20);
}
else if(i==1)
{
printf("child %d pid %d\n,runing..\n",i,getpid());
while(1)
sleep(1);
}
}
else
{
perrror("fork call failed");
exit(0);
}
return 0;
}
```
[![6.png](https://i.postimg.cc/FzDLrr6L/6.png)](https://postimg.cc/tnnTDjpq)
[![7.png](https://i.postimg.cc/mZwMNjrg/7.png)](https://postimg.cc/Z0WCJr3G)
[![8.png](https://i.postimg.cc/hPtmCmJb/8.png)](https://postimg.cc/Cd9d5zsz)


###进程间通信
进程间通信的简写是ipc,可以利用这种技术完成多个进程间的数据传递，信息收发
原始数据在进程第一阶段进行处理封装，再转发到进程第二阶段进行处理封装，再转发到进程第三阶段进行处理封装（处理完毕）最后得到目标数据
网络通信也是进程间通信
进程间通信方式有很多：匿名管道（pipe）,消息队列（posix，systemv）,内存共享映射（MMAP），信号（signal），套接字技术（socket），有名管道（FIFO）

进程A给进程B发消息：无法直接从用户层直接发，但进程的内核层是共享的，都是将用户层的数据通过内核层来发送
（绝大多数进程间通信都是利用内核层实现的）（内核层共享内存）
PIPE 匿名通道：
1.流通性（传输介质）
2.方向性
3.暂存能力（存储量很少）
A\-\>B；A先在用户层创建一个pipe（fds）（int fds[2]）函数，函数被调用后，在管道中创建一个缓冲区（PIPE\_BUFFER）(4K)环形队列（不同版本之间的管道大小不一样，旧：64K,新：4K），当管道创建成功后，系统会将读写管道的两个描述符传出到fds中，让用户可以读写管道
文件描述符应是最小的未使用的（3）（0：标准输入，1：标准输出，2：标准错误）
匿名管道只能在亲缘关系间的管道间用

[![9.png](https://i.postimg.cc/6p1t6NFB/9.png)](https://postimg.cc/NKTWbZgn)
```c
#include<stdio.h>
#include<unistd.h>
#include<string.h>
#include<stdlib.h>
#include<sys/wait.h>

#define MSG "Can u hear Me?"

int main(void)
{
int fds[2];
pipe(fds);
pid_t pid;
pid=fork();
if(pid>0)
{
printf("parent %d Send Msg\n",getpid());
close(fds[0]);
write(fds[1],MSG,strlen(MSG));
wait(NULL);
close(fds[1]);
}
else if(pid==0)
{
close(fds[1]);
char buffer[1024];
bzero(buffer,sizeof(buffer));
read(fds[0],buffer,sizeof(buffer));
printf("child Read MSG=%s\n",buffer);
close(fds[0]);
exit(0);
}
else
{
perror("fork call  failed");
exit(0);
}
return 0;
}
```
管道为空，写端未写数据，读端读取管道，读堵塞
管道为满，读端未读数据，写端写管道，写堵塞
写端关闭，如果管道有数据，读端读取数据管道剩余数据后再次读返回0，管道为空，直接返回0
管道读端关闭，写端尝试向管道写数据，系统回向写端进程发送SIGPIPE，杀死写端进程

\*编写一个服务端客户端模型(C5)，可以进行连接和基本的数据收发，客户端异常退出，服务器也异常退出，为什么?
send(int sockfd,buffer,len,MSG\_NOSIGNAL)//如果系统服务端写端)发送SIGPIPE号，可以利用MSG\_NOSIGNAL 忽略信号

匿名管道的缺点: 1.亲缘限制，只能亲缘进程可以使用其完成通信
2.默认情况下管道使用无格式字节流传输，需要用户自行封装
管道这种进程间通信方式，效率较好
在所有unix或linux系统，管道都是可以使用的，但是其他系统 ?

FIFO 有名管道
需先创建管道文件 mkfifo 测试管道//创建管道文件
p(管道文件) 管道文件没有存储能力，无法编辑
创建管道文件后，系统会在内存中创建一个管道缓冲区
管道文件被删除，系统立即清理管道缓冲区
[![10.png](https://i.postimg.cc/zvPz3bfX/10.png)](https://postimg.cc/5QLdRtvZ)
命名管道也是单工方式
```c
write:
#include<stdio.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<string.h>
#include<fcntl.h>
#include<unistd.h>
#include<stdlib.h>

#define MSG "189034352432534234"

int main(void)
{
//打开管道文件
int wfd =open("测试管道",O_WRONLY);
write(wfd,MSG,strlen(MSG));
printf("write %d write msg successly..\n",getpid());
close(wfd);
return 0;
}

read:
#include<stdio.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<string.h>
#include<fcntl.h>
#include<unistd.h>
#include<stdlib.h>

int main(void)
{
//打开管道文件
char buf[1024];
bzero(buf,sizeof(buf));
int rfd =open("测试管道",O_WRONLY);
read(rfd,buf,sizeof(buf));
printf("Read %d msg=%s\n",getpid(),buf);
close(rfd);
unlink("测试管道");//删除管道文件
return 0;
}
```
访问命名管道，必须满足两种权限，读写。才可以成功打开和使用管道，如果只有一种访问权限，会阻塞另一种权限

单进程只要满足两种权限（O\_RDWR)，可以直接打开和使用管道

有名管道使用时的特殊情况:
1.权限要求， 有名管道要求，满足两种访问权限才可以打开使用管道，否则要阻塞等待另一种
2.如果在一个进程中有多个读序列， 阻塞只会对第一个读序列生效，其他都会设置非阻塞
多线程为进程读取数据，一个线程阻塞等待即可，其他线程设置非阻塞立即返回，执行其他，避免阻塞开销
3.原子使用管道( 传输速度较慢，但是数据完整性比较好) 和 非原子使用管道(传输效率高， 无法保证数据完整性)
原子写管道：（每次写大小小于管道缓冲区大小）非原子写管道：（每次写大小大于管道缓冲区大小）
非原子访问请况下，系统不会控制流，只要管通绿冲区有余量，写端可以立即写入数据，传输效率高，但是读端读取数据后要校验完整性，邀免数据包的异常
不要频繁变更传输模型

MMAP文件共享映射
void * ptr =mmap(NULL,映射大小,PROT\_READ|PROT\_WRITE,映射方式,文件描述符,文件描述符，映射偏移量);
私有映射：拷贝映射，将映射文件的数据拷贝一份到映射内存，两份数据独立无关联
共享映射：同步映射，同步映射文件的数据映射一份给进程，两份数据建立sync同步机制，对一份数据的修改会立即更新给另一份
映射内存地址，如果传NULL，系统自动分配映射内存
一般是文件大小
映射内存权限 PROT\_READ|PROT\_WRITE|PROT\_EXEC|PROT\_NONE
共享映射(MAP\_SHARED) 私有映射 MAP\_PRIVATE
映射文件的描述符，映射时使用访问磁盘数据
映射偏移量，mmap支持便宜映射，每次映射一部分（适合处理大文件）
munmap(void \* ptr,映射大小)//释放映射内存
映射成功返回ptr,映射内存地址，失败返回MAP\_FAILED关键字
mmap要确定通信方向，一个负责编辑修改映射内存马，一个负责显示打印映射内存数据，不要让两映射同时修改访问映射内存，会导致出现数据异常
```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<unistd.h>
#include<sys/mman.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<fcntl.h>
int main(void)
{
int fd=open("MAp_File",O_RDWR);//注意文件名不要写错
int size;
size=lseek(fd,0,SEEK_END);//获取文件大小
int * ptr=NULL;
if((ptr =mmap(NULL,size,PROT_READ|PROT_WRITE,MAP_SHARED,fd,0))==MAP_FAILED)
{
perror("mmap call failed");
exit(0);
}
close(fd);
//修改映射内存数据，让它同步给文件
ptr[0]=0X34333231;//通过16进制来直接修改文件内容，16进制在存储时是倒着存储
nmap(ptr,size);
return 0;
}
```
mmap通过open时的权限来判别进程的身份
mmap是否可以读写映射，取决于文件打开权限，对要打开文件时有足够的权限，那么可以进行读写映射，映射的权限小于等于文件的权限
mmap读写效率最高
写端：打开映射文件，扩展空文件，共享映射，向映射内存导入数据
读端：打开映射文件，共享映射，打印内存数据
```c
写端：
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<unistd.h>
#include<sys/mman.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<fcntl.h>

typedef struct
{
 int id;
char date[1024];
}msg_t;

int main(void)
{
int fd=open("MAp_File",O_RDWR);
//扩展空文件
ftruncate(fd,sizeof(msg_t));
msg_t  * ptr=NULL;
if((ptr =mmap(NULL,sizeof(msg_t),PROT_READ|PROT_WRITE,MAP_SHARED,fd,0))==MAP_FAILED)
{
perror("mmap call failed");
exit(0);
}
close(fd);
//持续向映射文件内存写入数据
ptr->id=0;
bzero(ptr->date,1024);
while(1)
{
++(ptr->id);
sprintf(ptr->date,"test message,msg id %d",ptr->id);
sleep(1);
}
munmap(ptr,sizeof(msg_t));
return 0;
}

读端：
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<unistd.h>
#include<sys/mman.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<fcntl.h>

typedef struct
{
 int id;
char date[1024];
}msg_t;

int main(void)
{
int fd=open("MAp_File",O_RDWR);
msg_t * ptr=NULL;
if((ptr =mmap(NULL,sizeof(msg_t),PROT_READ|PROT_WRITE,MAP_SHARED,fd,0))==MAP_FAILED)
{
perror("mmap call failed");
exit(0);
}
close(fd);
//持续显示映射内存数据
while(1)
{
printf("msgid= %d,msg =%s\n",ptr->id,ptr->date);
sleep(1);
}
munmap(ptr,sizeof(msg_t));
return 0;
}
```
关于mmap的同步机制
硬盘中经常使用的数据加载到内存中，从而降低磁头的寻址频率，保护磁头，这种技术就叫高速缓存技术date\_cache
用户空间中有一块映射内存，它不在栈和堆，在库空间中，因为库空间具有弹性
高速缓存会将数据映射到映射内存（虚拟地址）
用户访问映射时会产生缺页中断，发生缺页中断会将高速缓存的数据拷贝放到物理内存中
当用户对数据就行修改访问时会产生脏页
当脏页被访问我完后将会脏页的数据重写回内存
[![11.png](https://i.postimg.cc/2yqPyGKh/11.png)](https://postimg.cc/0KstHYxy)


从文件中读取数据
read （用户从硬盘读取数据总共4次切换（来回），2次拷贝）
先将硬盘读取到DMA（缓存引擎）：DMA copy（可以不算到拷贝次数中）（预读数据）
DMA会将数据拷贝到内核缓冲区（date cache）（第一次）
内核缓冲区将数据拷贝到用户缓冲区（buffer）（第二次）
mmap(4次切换，1次拷贝)
mmap会在内核缓冲区和用户缓冲区之间就行内存映射
，而不是拷贝
mmap也可用于socket通信
只是硬盘换成了网卡，内核缓冲区换成了SOCKET缓冲区
网络上常用的拷贝技术（ZERO\_COPY)
零拷贝技术不是只零次拷贝而是只减少拷贝次数
SendFile
两个缓冲区直接映射（只适用文件传输）
[![12.png](https://i.postimg.cc/K863Xhmx/12.png)](https://postimg.cc/5Xm2vGHR)


使用mmap出现的异常
映射内存的大小不要大于文件实际大小，因为再映射时要加载文件大小来设置映射内存的可用大小的
再进行映射时， 一般要看映射文件大小，如果映射内存与映射文件大小不符， 再访问内存时产生总线错误，系统向进程发送SIGBUS,杀死进程
总线错误就跟溢出有关


进程间关系
亲缘关系
Linux 操作系统下，进程间的关系是强亲缘(父子)，弱亲缘(爷孙)
爷爷进程与孙子进程最低限度亲缘(继承关系)
强亲缘关系(父子进程)， 子进程被父进程创建， 子进程的任务被父进程指定，继承父进程数据，子进程结束后，父进程负责回收避免僵尸问题，整个子进程生命周期父进程全程参与
```c
clude<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<sys/fcntl.h>
#include<pthread.h>
#include<signal.h>
int main(void)
{
printf("app pid %d,app parent pid  %d\n",getpid(),getppid());
while(1)
{
sleep(1);
}
return 0;
}
```
[![13.png](https://i.postimg.cc/dtHwZ2ff/13.png)](https://postimg.cc/bstKKtp0)
Process Group组关系
进程组的销毁不跟组长是否存在有关，只有组中最后一个进程结束或转移，没有进程才能销毁
getpid()//返回进程pid
getppid()//返回进程父进程id
getpgrp()//返回进程进程组id
```c
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<sys/fcntl.h>
#include<pthread.h>
#include<signal.h>
int main(void)
{
pid_t pid;
int i;
for(i=0;i<3;i++)
{
pid=fork();
if(pid==0)
break;
}
if(pid>0)
{
printf("parent  pid %d ppid %d pgrp %d\n",getpid(),getppid(),getpgrp());
while(1)
sleep(1);
}
else if(pid==0)
{
printf("child %d pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
while(1)
sleep(1);
}
else
{
perror("fork call failed");
exit(0);
}
return 0;
}
```

