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
进程组的销毁，组中的最后一个进程，结束戏转移， 进程组种没有进程时系统会择放进程组
就近原则，子进程被创建后默认归纳到父进程同组成为组员
子进程一定是父进程的组员进程，这个既念是错的，因为组员是可以变动的，可以将组员组员进程转移到其他组中去
组长是不允许转移的
组长进程无法创建进程组，组员进程可以创建新租，脱离原有的进程组，成为新的组长
子进程独立新组后，亲缘关系不变，子进程结束后由父进程回收（子进程脱离原有进程组，父进程通过waitpid进行跨组回收）
setpgid(pid\_t pid,pid\_t gid)//可以让组员创建新组，也可以将一个组员转移到其他组
eg:setpgid(1000,1000)setpgid(1000,5000)//转移时目标组必须存在，需要对目标组有访问权限
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
if(i==2)
{
printf("child %d  pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
printf("child %d pid %d create process group\n",i,getpid());
setpgid(getpid(),getpid());//创建组
printf("child %d  pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
while(1)
sleep(1);
}
printf("child %d  pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
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
process session 会话关系
会话是一种终端进程管理的组织结构
bash是会话发起者，剩下的无论是父还是子都是会话参与者
pid==gid==sid//则说明它是会话发起者
pid==gid//说明它是父进程
会话和进程组的区别：当会话发起者结束会话时，系统会以组的形式杀死一组（只杀一组），杀死的是终端子进程的那一组，终端子进程必然被杀死，但终端子进程的子进程可以创建一个新组从而存活,并不意味着脱离会话
```c
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
printf("child %d  pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
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
```linux
ps aux
```
让子进程脱离会话，创建新会话，避免被终端杀死（简称脱离控制终端）
```c
getsid(getpid())//返回会话sid
setsid()//创建进程组并创建新会话，脱控制终端
```
[![14.png](https://i.postimg.cc/XvjSTnTS/14.png)](https://postimg.cc/G455DnLq)
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
if(i==0)
{
//创建新进程组，避免被会话杀死
setpgid(getpid(),getpid());
while(1)
sleep(1);
}
printf("child %d  pid %d ppid %d pgrp %d\n",i,getpid(),getppid(),getpgrp());
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
```linux
ps ajx//专门查看进程间关系的
```
orphan 孤儿进程
当父进程因特殊原因消失时，子进程会被托管给一个专门托管孤儿进程的一个进程
原因：如果没有托管处理机制，那么就会出现无法被处理的僵尸进程
孤儿进程这种活态进程的免害是有弹性的，取决于孤儿进程的作业，如果孤儿进程被设置大量频紫的申请占用系统资源，那么这种孤儿进程危害极大
子进程一旦被托管，那么托管进程只负责回收子进程结束后的资源，不对孤儿进程就行管理
孤儿进程是异常多进程的残留，会影响新进程的创建与使用
开发者创建父子进程模型，让父进程退出，子进程变为守护进程
[![15.png](https://i.postimg.cc/pL2Fr17Q/15.png)](https://postimg.cc/Tp4wHQTh)
这个模型是同组下的检测处理
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
pid=fork();
if(pid>0)
{
printf("parent pid %d\n",getpid());
sleep(10);
exit(0);
}
else if(pid==0)
{
printf("child pid %d ppid %d\n",getpid(),getppid());
sleep(11);
while(1)
sleep(1);//子进程变为孤儿进程
}
else
{
perror("fork call failed");
exit(0);
}
return 0;
}
```
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
pid=fork();
if(pid>0)
{
printf("parent pid %d\n",getpid());
sleep(10);
exit(0);
}
else if(pid==0)
{
while(1){
printf("child pid %d ppid %d\n",getpid(),getppid());
sleep(1);
}
//子进程变为孤儿进程
}
else
{
perror("fork call failed");
exit(0);
}
return 0;
}
//这种可以在终端上直观的体现
```
这种可以继续输入命令，命令能正常执行
deamon process 守护进程/精灵进程（shell设置进程开机启动）
守护进程是经典的后台服务进程，持续在后台运行完成特殊服务，执行特定功能，不干预前台任务
普通的软件进程随用户的使用持续， 生命周期较短
守护进程生命周期较长， 开机启动关机结束， 持续服务于后台
守护进程不能持续占用系统资源(cpu，内存等等)， 长时间处于低开销模式
守护进程的工作模式: 间隔执行(sleep)，定时启动，条件触发 ，低消模式(大多数时间进程处于睡眠态)
后台服务进程不允许访问前台，标准输入标准输出不使用，标准出错(dup2实现重定向)
守护进程其实是孤儿进程， 人为的孤儿进程

守护进程的实现流程
1.fork创建子进程，父进程退出
2.子进程创建新会话，脱离控制终端
3.关闭无用的描述符，将表标准出错流重定向
4.修改进程工作路径，改为根目录(普通用户不要改为根目录，不然会没有权限)chdir("./");
5.修改目标主机进程umask文件权限掩码，改为0002或0000
6.守护进程的核心工作
7.守护进程退出处理释放执行过程中申请的资源数据守护进程结束时主动释放
1.创建一个 Daemon process 文件夹 ， 在此文件夹中开发守护进程
2.编译后，守护进程的程序名为Daemon\_process
3.守护进程创建日志文件，文件名为 time.log
4.守护进程间隔执行，每间隔3s向日志文件中写入系统时间
5.守护进程后台运行
```c
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<fcntl.h>
#include<string.h>
#include<signal.h>
#include<time.h>

void Deamon_business(void)
{
int fd;
time_t tm;//时间种子类型
char time_buffer[1024];
bzero(time_buffer,sizeof(time_buffer));
if((fd=open("time.log",O_RDWR|O_CREAT,0664))==-1)
{
perror("open failed");
exit(0);
}
while(1)
{
tm=time(NULL);
ctime_r(&tm,time_buffer);
write(fd,time_buffer,strlen(time_buffer));
bzero(time_buffer,sizeof(time_buffer));
sleep(3);
}
close(fd);
}
void Deamon_create(void)
{//创建子进程，父进程退出
pid_t pid;
pid=fork();
if(pid>0)
{
exit(0);//父进程直接退出
}
else if(pid==0)
{
//创建新会话，脱离中断
setsid();
//改变进程工作路径
chdir("./");
//修改进程umask
umask(0002);
//关闭无用描述符
close(STDIN_FILENO);
close(STDOUT_FILENO);
//重定向STDERR_FILENO

//执行守护进程的工作
Deamon_business();
//守护进程的退出处理（释放内存）

}
else
{
perror("fork call failed");
exit(0);
}
}

int main(void)
{
Deamon_create();

return 0;
}
```
```c
STDIN\_FILENO//标准输入流读取外部数据
STDOUT\_FILENO//标准输出流显示数据打印到显示器上
STDERR\_FILENO//标准错误流，通过标准输出流会打印到显示器上
```c
include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<fcntl.h>
#include<string.h>
#include<signal.h>
#include<time.h>

void Deamon_business(void)
{
int fd;
time_t tm;//时间种子类型
char time_buffer[1024];
bzero(time_buffer,sizeof(time_buffer));
if((fd=open("fsdf45af",O_RDWR))==-1)
{
perror("open failed");
exit(0);
}
while(1)
{
tm=time(NULL);
ctime_r(&tm,time_buffer);
write(fd,time_buffer,strlen(time_buffer));
bzero(time_buffer,sizeof(time_buffer));
sleep(3);
}
close(fd);
}
void Deamon_create(void)
{//创建子进程，父进程退出
pid_t pid;
pid=fork();
if(pid>0)
{
exit(0);//父进程直接退出
}
else if(pid==0)
{
//创建新会话，脱离中断
setsid();
//改变进程工作路径
chdir("./");
//修改进程umask
umask(0002);
//关闭无用描述符
close(STDIN_FILENO);
close(STDOUT_FILENO);
//重定向STDERR_FILENO
int fd=open("ERROR_FILE",O_RDWR|O_CREAT,0664);//创建重>定向错误文件
dup2(fd,STDERR_FILENO);//重定向
//执行守护进程的工作
Deamon_business();
//守护进程的退出处理（释放内存）

}
else
{
perror("fork call failed");
exit(0);
}
}

int main(void)
{
Deamon_create();

return 0;
}
```
[![16.png](https://i.postimg.cc/hvXqBwkJ/16.png)](https://postimg.cc/Cnp2CvLY)
开机启动
 shell脚本写完直接跑，不需要去启动
```linux
#!/bin/bash

date//查看日期

ls 

ps aux
```
```linux
sudo chmod 0775 shell脚本名//0775代表执行权限
```
启动块信息最好粘电脑自带的，要注意空格和#
写完shell脚本后要通过命令复制一份到/etc/init.d/中
```linux
sudo update-rc.d shell_start start 99 2.
//删除命令：
sudo update-rc.d shell remove
```
信号
信号是linux系统下的经典技术
一般操作系统利用信号杀死违规进程，典型进程干预手段， 信号除了杀死进程外也可以挂起进程
kI -l #看系统支持的信号
32,33号预留给线程库NTPL
两种信号，经典信号/实时信号
1-31 是unix经典信号，软件开发工程师使用，例如进程通信，信号浦捉等等
34-64 是盘定义信号，一般驱动开发使用，偏底层
[![17.png](https://i.postimg.cc/jjfxkKCk/17.png)](https://postimg.cc/HJp1VqwQ)
ctl+/(SIGOUIT/3) 系统向唯一的前台进程发送3号信号，杀死目标进程
ctl+z(SIGSTP/20) 系统向唯一的前台进程发送20号信号， 挂起目标进程
```linux
^z//挂起目标进程
jobs//查看手动挂起的进程
fg 1//将挂起的进程让它运行
bg 1//让挂起的进程后台运行
```
2,命令发送信号
```linux
kill -signo pid //此命令可以向任意进程发送任意信号
```
3.函数发送信号
```linux
//专用头文件：
#include<signal.h>
kill(pid_t pid,int signal)//#向任意进程发送任意信号
raise(int signo) //#向自身发送任意信号
void abort(void) //#向自身发送SIGABRT/6信号
```
```c
#include<signal.h>
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
//kill -signo pid
// ./mykill signo pid
int main(int argc, char ** argv)
{
if(argc<3)
{
printf("pram Failed,TryAgain..\n");
exit(0);
}
kill(atoi(argv[2]),atoi(argv[1]));
return 0;
}
```

4.硬件异常产生信号
对只读内存进行写操作，属于违规操作硬件，系统向违规进程发送 SIGSEGV(11)信号，杀死违规进程 
SIGSEGV信号可能是系统发出的，也有可能是其他用户发出的
SIGBUS（总线错误）：越界访问，无效访问内存，系统向违规进程发送SIGBUS（7）信号，杀死违规进程
SIGFPE(浮点数例外),cpu违规运算，运算异常，系统向违规进程发送SIGFPE(8)，杀死进程

```c
#include<signal.h>
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
//kill -signo pid
// ./mykill signo pid
int main(int argc, char ** argv)
{
char * str="hell";
str="xxxx";
str[0]='H';
kill(atoi(argv[2]),atoi(argv[1]));
return 0;
}
```
5.软条件触发信号
软件能发信号，在使用某个组件时，例如定时器，窥时到时，能发软条件，系统向进程发送信号
 [![18.png](https://i.postimg.cc/6p4bPtxL/18.png)](https://postimg.cc/qN0GhfRz)
管道读端结束，写端向管道写数据 (触发软条件，)系统向写端进程发送SIGPIPE13信号杀死写端进程
信号的三大行为，与五种默认处理动作
SIGNAL
SIG\_DFL 默认行为：TERM//直接杀死目标进程，sigkill,slgint
CORE//直接杀死进程，但是转储核心处理文件(dump core)，SIGQUIT，SIGSEGV SIGFPE SIGBUS
IGN//通知国收信号 SIGCHLD,忽路信号。 发到进程不会影响进程
STOP//挂起进程,SIGSTP，SIGTSTP
CONT//唤醒进程，SIGCONT
信号处置进程后， 可以通过结果分析信号的默认动作
5种默认处理动作
SIG\_IGN 忽略行为：NULL 忽略行为没有处理动作，直接丢奔，不会影响进程
忽略行为的优先级比动作要高
SIG\_ACTION 捕捉行为（自定义动作）：捕捉行为可以实现， 信号绑定自定义任务
信号触发， 执行捕捉函数，执行自定义任务
捕捉技术在开发中普遍使用

让信号失效的三种方式：屏蔽，忽略，捕捉
系统保留高权级信号， 这类信号无法被屏蔽， 捕捉和忽略，服务于内核，只要发出必然递达
SIGKILL(9)，无法被屏蔽，捕捉，忽略，只要发出必然杀死
SIGSTOP(19)无法被屏蔽，捕捉怨略， 只要发出必然挂起

信号的传递过程：
信号集，是一个位图，每一位表示一个信号，位码是0或1
信号无法通过未决信号集，位码是1， 此信号直接丢弃
如果信号通过未决信号集，系统将对应的位码设置1，标记为未决态信号，表示此信号正在传送，还未处理
HANDLER信号选择行为动作处置进程(信号处理流程)
屏藏宇信号集，用户自行设置，可以屏蔽阻塞信号，使其无法递达
信号屏蔽字对应的位变为1，可以实现阻塞信号
如果信号通过屏蔽字，进入handler处理流程，系统会将来决信号集对应位码翻转回0，表示从来决态信号切为递达态信号
信号屏蔽是延迟处理,此信号未消失， 某一刻屏蔽解除， 此信号马上递达，处置进程
前30个信号不支持队列，后30个信号支持队列，因为前30个信号是kill杀死进程用的一个就行，后30个是开发使用的
[![19.png](https://i.postimg.cc/sx77SjBK/19.png)](https://postimg.cc/vx84wdt6)

信号屏蔽实现：
```c
#include <signal.h>
sigset_t oldset
sigset_t set; //信号集类型
sigemptyset(sigset_t*set);//将set信号集种所有位初始化为0
sigfillset(sigset_t* set);//将set集合中所有位初始化为1
sigaddset(sigset_t* setint signo)//将set集合种某个信号的对应位设置为1
sigdelset(sigset_t*set,int sino); //将set集合中某个信号的对应位设置为0
bitcode = sigismember(sigset_t*set,int signo); //查看某个信号集种，对应信号的位码并直接返回0或1
sigprocmask(SIG SETMASK,sigset_t* newset，&oldset): //可以替换进程信号集,并将原有的oldset传出保存，便于复位
int how = SIG_SETMASK(替换覆盖)SIG_BLOCK(位或) SIG_UNBLOCK(取反求与)
```c
#include<stdio.b>
#include<unistd.h>
#include<string.h>
#include<signal.h>
int main(void)
{
sigset_t set,oset;
sigemptyset(&set);//初始化 O
sigaddset(&set,SIGINT);//设置屏蔽 SIGINT
sigaddset(&set,SIGQUIT);//设置屏蔽 SIGQUIT
sigaddset(&set,SIGKILL);//设置屏蔽 SIGKILL
sigprocmask(SIG_SETMASK,&set,&oset);
while(1)
sleep(1);
return 0;
}
```
查看信号的屏蔽情况
如果想查看信号的实时情况，需要看未决信号集
信号已经被发出，递达进程，进程种被屏蔽，要观察这种已触发被屏蔽的信号只能查看未决信号集
虽然未决信号集不能去写，但可以通过读来完成一些开发的应用
获取进程的未决信号集， 而后输出未决的每一位， or 1，查看信号屏蔽
sigpending(&pset); //调用此函数，系统将进程的未决信号集传出到pset中
使用遍历循环结合sigismember,查看每一位的情况并输出
```c
#include<stdio.h>
#include<unistd.h>
#include<string.h>
#include<signal.h>
//查看信号的屏蔽情况，遍历打印来未决信号集
void print_pest(sigset_t pest)
{
int i=1;
for(i;i<32;i++)
{
if((sigismember(&pest,i)))
{
putchar('1);
}
else
{
putchar('0');
}
}
putchar('\n');
}
int main(void)
{
sigset_t set,oset，pest;
sigemptyset(&set);//初始化 O
sigaddset(&set,SIGINT);//设置屏蔽 SIGINT
sigaddset(&set,SIGQUIT);//设置屏蔽 SIGQUIT
sigprocmask(SIG_SETMASK,&set,&oset);
while(1)
{
sigpending(&pest);
print_pest(pest);
sleep(1);
}
return 0;
}
```
信号行为修改
struct sigaction act; //信号行为结构体
act.sa\_handler = SIG\_DFL| SIG\_IGN|传递函数指针-> 自定义捕提函数o
act.sa\_flags = 0 /此成员与行为接口定，如果使用a\_handler 那sa\_flags为0，如果使用sa\_sigaction,flags为SA\_SIGINFO
act.sa\_mask//sigset\_t 信号集类型，为临时屏蔽字使用sigemptyset初始化
sigaction(int signo,struct sigaciont \* newact,struct sigacion\* oldact);//替换进程的信号行为结构体，用newact替换，传出oldact(进程原有结构体）
```c


#include<stdio.h>
#include<unistd.h>
#include<string.h>
#include<signal.h>

//自定义捕捉函数
//sa_handler=void(*sa_handler)(int)
//sa handler是一个函数指针类型，但是捕捉函数定义必须与其一致
void sig_do(int n)
{
//系统调用捕捉函数时，系统向n传捕捉的信号编号
printf("SIGINT %d 捕捉成功 \n",n);
}

//修改信号行为

int main(void)
{
struct sigaction act,oact;
//act.sa_handler=SIG_DFL//默认行为
//act.sa_handler=SIG_IGN//忽略行为
act.sa_handler=sig_do;//捕捉行为
act.sa_flags=0;
sigemptyset(&act.sa_mask);
sigaction(SIGINT,&act,&oact);//行为替换
while(1)
{
sleep(1);
}
return 0;
}
```
这些行为只对当前进程生效
```c
#include<stdio.h>
#include<unistd.h>
#include<string.h>
#include<signal.h>

void sig_do(int n)
{
int flag=2;
while(flag--)
{
printf("flag %d\n",flag);
sleep(1);
}
}

//修改信号行为

int main(void)
{
struct sigaction act,oact;
act.sa_handler=sig_do;//捕捉行为
act.sa_flags=0;
sigemptyset(&act.sa_mask);
sigaction(SIGINT,&act,&oact);//行为替换
while(1)
{
sleep(1);
}
return 0;
}
```
为了防止一个信号被捕捉时，下一个信号在上一个信号没处置完时被捕捉，系统会将屏蔽信号集对应的位置置为1
[![20.png](https://i.postimg.cc/prLwPfXD/20.png)](https://postimg.cc/34zSBDGR)


DUMP CORE
信号的默认行为中有五种处理动作
TERM CORE IGN STOP CONT
重接杀死进程
杀死进醒的同时，转储核心文件
如果进程因为硬件异常被系统杀死，那么会(Dump core)，错误原因 xxx(核心已转储)

```c
oid err(void)
{
char str ="failed";
str[0]='F';
}
int main(void)
{
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
printf("Xsasdad\n");
err();
return 0;
}
```
```linux
ulimit -a//查看系统资源
```
信号回收
wait() //阻塞回收(主动回收)
waitpid()//非阻赛回收 (主动回收)
信号回收 (被动回收方案)
[![21.png](https://i.postimg.cc/vHKrykr0/21.png)](https://postimg.cc/mtQzNd69)
捕捉函数执行流程
[![22.png](https://i.postimg.cc/jdtLnbT8/22.png)](https://postimg.cc/7btxjjf7)
 问题：什么是用户层，什么是内核层
 答：CPU在完成不同任务下的不同权限（CPU在一些情况下会自封一部分权限去限制访问某些程序）
一般main先执行 过程中产生信号，系统执行捕捉函数，捕捉函数先执行完，稍后回到主函数继续执行
Level3，最低圾cpu权限，访问大部分系统设备都受限(用户层)
level 0。最高吸cpu权限，可以访问所有设备和资源(内核吸)
[![23.png](https://i.postimg.cc/vHrRRjSf/23.png)](https://postimg.cc/Tp3Ngkx3)


关于捕捉函数的可重入不可重入问题
全局安量inta=1024，此数据被捕提函数和主函数同时使用全局安量会引发不可重入问题
全局链表关于insert问题
使用全局资源或静态资源的函数成为不可重入函数，这种函数信号捕捉函数与主函数同时使用会引发异常
可重入概念， 访问的数据也好， 函数也罢， 都不访问共享资源，不会引发冲突， 这种函数成为可重入函数，信号使用可重入内容是安全的 
信号捕捉开发不允许使用不可重入内容
满提函数和main函数都是使用全局链表的insert操作，必然引发内存泄规链表中的节点异常
[![24.png](https://i.postimg.cc/Qx4Dhq90/24.png)](https://postimg.cc/hfd60T0d)
时序竞态（）
进程间通信
sigqueue(pid\_t pid,int signo,struct union sigval val)////向任意进程发送任意信号并且携带自定义数据
val.sival\_int =整数数据
val.sival\_ptr =void \* 地址数据
信号通信亲缘间使用比较简单,但是不相干的进程要想办法获取目标pid
父进程关于子进程pid的问题，可以将pid存储在全局变量，便于捕捉函数使用，也可以使用getpid()+1,定位子进程
[![25.png](https://i.postimg.cc/mgMmFD60/25.png)](https://postimg.cc/PCXWgtH4)

```c
#include<stdlib.h>
#include<stdio.h>
#include<unistd.h>
#include<signal.h>
#include<string.h>
pid_t child_pid;
void Parent_sig(int n,siginfo_t * info , void * arg)
{
//捕捉 SIGUSR2信号
printf("Parent_pid [%d],%d\n",getpid(),info->si_int);//显示数据
union sigval val;
val.sival_int=++(info->si_int);
sigqueue(child_pid,SIGUSR1,val);
usleep(50000);
}
void Child_sig(int n ,siginfo_t * info , void * arg)
{
//捕捉 SIGUSR1信号
printf("Child_pid [%d],%d\n",getpid(),info->si_int);//显示数据
union sigval val;
val.sival_int=++(info->si_int);
sigqueue(getppid(),SIGUSR2,val);
usleep(50000);
}
int main(void)
{
pid_t pid;
//父进程捕捉设定，捕捉SIGUSR2信号
struct sigaction act,oact;
act.sa_sigaction = Parent_sig;
act.sa_flags = SA_SIGINFO;
sigemptyset(&act.sa_mask);
sigaction(SIGUSR2,&act,&oact);
//父进程屏蔽SIGUSR1，将屏蔽字继承给子是程
sigset_t set,oset;
sigemptyset(&set);
sigaddset(&set,SIGUSR1);
sigprocmask(SIG_SETMASK,&set,&oset);
pid = fork();
if(pid > 0)
{
//第一次信号发送(携带数据
union sigval val;
val.sival_int = 1;
child_pid=pid;
sigqueue(pid,SIGUSR1,val);
while(1)
sleep(1);//等待信号
}
else if(pid == 0)
{
//设置捕捉
struct sigaction act,oact;
act.sa_sigaction = Child_sig;
act.sa_flags = SA_SIGINFO;
sigemptyset(&act.sa_mask);
sigaction(SIGUSR1,&act,&oact);
//解除屏蔽
sigprocmask(SIG_SETMASK,&act.sa_mask,NULL);
//等待信号
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

时序竞态（）
alarm(10)定时进程，当定时到时，系统向定时进程发送SIGALRY信号
CPU定时与进程无关
SIGALRM信号默认的动作是TERM.会苏死目标进程，一定要让其失效
pause 察觉信号涣醒，挂起过程中， 察觉到任意一个信号立即决醒，此信号必须要有处理动作这意味着，在定时到时前，如果有信号先于ALRM信号到达，pause会被误唤醒
使用信号捕捉让信号失效，并且有处理流程。可以被pause察觉，捕捉函数空调用即可。设有附加功能
```c
void Pause(void)//执行立即挂起当前进程
```
[![26.png](https://i.postimg.cc/66Hdrfyg/26.png)](https://postimg.cc/23Zbmvd7)
```c
void sig_alarm(int n)
{
//null

}
unsigned int mysleep(unsigned int seconds)
{
unsigned int val;
//捕捉设定
//屏蔽SIGALRM
sigset_t set,oset;//[14][1]
sigemptyset(&set);
sigaddset(&set,SIGALRM);
sigprocmask(SIG_SETMASK,&set,&oset);//[14][1]
struct sigaction act,oact;
act.sa_handler = sig_alarm;
act.sa_flags = 0;
sigemptyset(&act.sa_mask);//
sigaction(SIGALRM,&act,&oact);
val = alarm(seconds);
sleep(3);//----->在sleep期间,信号触发，处理SIGALRM信号
//解除屏蔽同时挂起进程
sigsuspend(&act.sa_mask);//[14][0]
//这给时序问题提供一个解决方案，考虑原子方法，将关键步骤变为不可分调的原子操作，
避免一些异常
//pause();//挂起进程
return val;
}
int main(void)
{
while(1)
{
printf("two seconds..\n");
mysleep(2);
}
return 0;
}
```
实现进程的外部控制
[![28.png](https://i.postimg.cc/VNbrwFGS/28.png)](https://postimg.cc/XZ47c903)
```c
void sig_stop(int n)//捕捉sigusri信号
{
pause();
}

void sig_cont(int n)
{
//null

}
void server_sigaction(void)
{
struct sigaction act,bct,oact;
act.sa_handler =sig_stop;
act.sa_flags = 0;
sigemptyset(&act.sa_mask);
sigaction(SIGUSR1,&act,&oact);
bct.sa_handler = sig_cont;
bct.sa_flags = 0;
sigemptyset(&bct.sa_mask);
sigaction(SIGUSR2,&bct,NULL);
}
void out_pid(void)
{
int fd;
char id[10];
fd=open("server_config.conf",O_RDWR|O_CREAT,0664);
pid_t pid=getpid();
sprintf(id,"%d",pid);
write(fd,id,strlen(id));
close(fd);
}
int main(void)
{
server_sigaction();//捕捉设定
out_pid();//抛出进程id到文件
while(1)
{
//服务器主要业务
printf("Server service Demo , version 0.0.1 , Listen epoll , Wait Client...\n");
sleep(1);
}
}
```
```shell
#!/bin/bash


#echo $1 $2 $3
PID=`cat server_config.conf`
echo $PID

if [ $1 = "stop" ]
then kill -10 $PID
elif [ $1 = "cont" ]
then kill -12 $PID
else print "Control Shell Failed\n"
fi
```
关于阻塞函数和信号处理冲突
阻塞函数处于等待状态，等待系统通知或事件消息
[![29.png](https://i.postimg.cc/cC1MRMnL/29.png)](https://postimg.cc/0M3wxSnT)
```c
//信号引发的中断
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
#include<sys/types.h>
#include<sys/stat.h>
#include<sys/fcntl.h>
#include<pthread.h>
#include<signal.h>
#include<string.h>
#include<errno.h>

void sig_int(int n)
{
printf("成功捕捉SIGINT %d 信号\n",n);
}
int main(void)
{
int len;
struct sigaction act,oact;
act.sa_handler = sig_int;
act.sa_flags = 0;
sigemptyset(&act.sa_mask);
sigaction(SIGINT,&act,&oact);
char buf[1024];
bzero(buf,sizeof(buf));
tryagain:
while((len = read(STDIN_FILENO,buf,sizeof(buf)))>0)
{
write(STDOUT_FILENO,buf,strlen(buf));
bzero(buf,sizeof(buf));
}
if(len == -1)
{
if(errno == EINTR)
{
printf("read函数被强制中断，TryAgain..\n");
goto tryagain;
}
}
return 0;
}
```
线程
线程基础概述
经典的并发模型多进程模型，占用大量的内存开销， 庞大的进程间调度开销，提供一种开销更小，更轻量的并发解决方案，多线程技术
线程在进程中，与进程共享资源和数据，进程是容器，线程是执行单元，进程退出可能导致所有线程退出
不支持线程技术的操作系统可以忽略线程概念，进程是调度单位
多线程操作系统下， 进程是内存管理单位，线程才是唯一的调度单元
线程就是寄存器和栈
[![30.png](https://i.postimg.cc/tC5WrLNC/30.png)](https://postimg.cc/HVrrnvNf)
多进程模型
[![31.png](https://i.postimg.cc/SR4V9ckZ/31.png)](https://postimg.cc/R6Pc563f)
多线程模型
[![32.png](https://i.postimg.cc/3x0pKdHW/32.png)](https://postimg.cc/Jsmtx70W)
线程的CPU分配
Kernel\_Thread内核级线程
操作系统中每创建一个线程，系统都会为其创建一个内核对象， 此线程系统可以识别支持，会为线程执行资源 (时间片)
[![33.png](https://i.postimg.cc/1X0s7d5S/33.png)](https://postimg.cc/BPvrXMK7)
用户级线程User\_Thread
用户级线程，虽然系统不会主动分配资源，但系统线程放弃，通过就近原则，用户级线程就可以用到资源
用户及线程，可以利用第三方库的形式在不支持线程技术的系统下安装和使用线程， 用户级线程的调度开销更小，因为大部分的操作都在用户层完成，无需内核干预
[![34.png](https://i.postimg.cc/FRXCRK1Q/34.png)](https://postimg.cc/Mctm3qys)
Linux操作系统下， 线程就是轻量级进程，每个进程分配一个LWP
在linux操作系统下 所有的度单位都是进程，淡化线程概念
进程的蜕化
进程内存资源独占，不予其他人共享， 进程是独立的调度单位(无需考虑线程问题)
讨论和分析的蜕化， 讨论线程，进程的讨论变为 主线程和普通线程的分析和讨论
进程中出现了多个执行单元， 讨论考虑线程问题
多线程在进程中的资源共享
PCB是共享资源
栈空间非共享，每个线程创建后，会分配8M线程栈
库资源共享  信号的处理行为共享(某个线程改变信号行为)，对所有线程生效
共享堆空间   信号屏蔽字非共享，普通线程据有独立的研藏字，拷贝继承于主线理
全局资源共享  TCB非共享，每个线程据有独立的线程控制块，独立的tid
代码段共享
文件描述符共享
信号行为共享
线程开发相关的API接口
NPTL线程库是典型的内核级线程库， 创建的线程可以被系统识别分配cpu资源(轻量级进程)(nativ Posix thread library)
ps aux 进程查看 pa ajx 进程关系查看 ps -eLf所有线程查看 ps -Lf pid进程中线程查看
每个线程都会被系统分配lwp 调度编号， 便于系统管理调度线程， 但是线程拥有独立的tid 线程id
```c
#include<pthread.h>
pthread_t tid;//线程tid类型
int err=pthread_create(pthread_t * tid , NULL , void * (* thread_job)(void *) , void * arg)//线程创建并指定任务
```
关于线程函数的错误处理，线程函数会返回错误号(err > 0)，使用char\* errstr = strerror(err)
调用线程时要保证进程存活
在使用线程时都需要链接库（gcc 文件名 -l库名 -o app）
```c
void * thread_job(void * arg)//普通线程工作
{
printf("普通线程被创建，参数为 %d\n",*(int *)arg);
return NULL;
}
int main(void)//主函数是全控线程的任务
{
pthread_t tid;
int code = 1024;
pthread_create(&tid,NULL,thread_job,(void*)&code);
printf("主线程创建普通线程成功... \n");
while(1)
sleep(1);
return 0;
}
```
```c
void * thread_job(void * arg)//普通线程工作
{
//printf("普通线程被创建，参数为 %d\n",*(int *)arg);
while(1)
sleep(1);
return NULL;
}
int main(void)//主函数是全控线程的任务
{
pthread_t tid;
int code = 1024;
int flags=0;
int err;
while(1)
{
if((err=pthread_create(&tid,NULL,thread_job,(void*)&code))>0)
{
printf("pthread create call failed:%s\n",strerror(err));
exit(0);//进程退出
}
printf("flags %d\n",++flags);
}
return 0;
}
```
pthread\_t tid = pthread\_self(void); //成功返回当前线程tid
主线程通过pthread\_reate 创建普通线程，成功传出td 与普通线程自身利用pthread\_self()得到的tid 值相等但是进程状态不相等，因为pthread\_self()获取tid时可以保证当前的有效性
pthread\_join(pthread\_t tid,void \*\* reval): //线程回收函数，可以回收线程资源的同时获取线程的返回值 经典的阻塞回收函数，会一直等待曾通线程结束后，进行回收
pthread\_cancel(pthread\_t tid)://指定线程tid. 取消结束线程
void pthread\_testcancel(void)产生一次系统调用(一般配合pthread\_cancel使用)
```c
void * thread_job(void * arg)//普通线程工作
{
//printf("普通线程被创建，参数为 %d\n",*(int *)arg);
while(1)
{
printf("普通线程Runing...\n");
sleep(1);
}
return (void*)126;
}
int main(void)//主函数是全控线程的任务
{
pthread_t tid;
int code = 1024;
int flags=0;
int err;
void * reval=NULL;
if((err=pthread_create(&tid,NULL,thread_job,(void*)&code))>0)
{
printf("pthread create call failed:%s\n",strerror(err));
exit(0);//进程退出
}
printf("Mondter thread 0x%x,普通线程 id  0x%x\n",(unsigned int)pthread_self(),(unsigned int)tid);
sleep(5);
pthread_cancel(tid);
//thread_join(tid,&reval);
//printf("Mondter exit code %ld\n",(long int)reval);
while(1)
sleep(1);
return 0;
}
```
```c
void * thread_job(void * arg)//普通线程工作
{
//printf("普通线程被创建，参数为 %d\n",*(int *)arg);
while(1)
{
//printf("普通线程Runing...\n");
//sleep(1);
pthread_testcancel();
}
return (void*)126;
}
int main(void)//主函数是全控线程的任务
{
pthread_t tid;
int code = 1024;
int flags=0;
int err;
void * reval=NULL;
if((err=pthread_create(&tid,NULL,thread_job,(void*)&code))>0)
{
printf("pthread create call failed:%s\n",strerror(err));
exit(0);//进程退出
}
printf("Mondter thread 0x%x,普通线程 id  0x%x\n",(unsigned int)pthread_self(),(unsigned int)tid);
sleep(5);
pthread_cancel(tid);
thread_join(tid,&reval);
printf("Mondter exit code %ld\n",(long int)reval);
while(1)
sleep(1);
return 0;
}
```
线程指定退出码时不允许使用-1.保留给pthread\_caneel
信号处理的三个切换条件，系统调用，软件中断， 软件异常
cancel取消事件的处理条件，必须有系统调用
[![35.png](https://i.postimg.cc/pTs9xwFH/35.png)](https://postimg.cc/S2zQftdT)
//回首态线程，这种状态是线程的默认状态，这种线程结束后必须手动回收 pthread\_join
//这种线程结来后系统自动回收线程资源，分离态线程，无需用户干预 
修改线程调出状态，从回收态改为分离态， 此操作不可逆， 不能将分离线程变为回收
如果对一个分离态线程进行回收操作， pthread\_join 会失败返回
对一个已经处于回收阶段(join已经开始阻塞等待了)的线程设置分离，分离设置失败
一个自行回收，一个系统回收， 一个可以得到线程退出码，一个无法获取
```c
pthread_detach(pthread_t tid);//将一个线程设置为分离态线程
pthread_exit((void *)126); //线程退出函数， 结束当前线程， 与进程无关，退出码可以被join获取
```
退出方式
[![36.png](https://i.postimg.cc/J06PD7s4/36.png)](https://postimg.cc/jnfzBb6G)
线程属性
```c
pthread_create(&tid , pthread_attr_t * attr , thread_job , NULL):
pthread_attr_t attr: 线程属性类型
```
[![37.png](https://i.postimg.cc/5N9jgrtF/37.png)](https://postimg.cc/4nMJNBVJ)

最后一个32位系统有
线程栈的大小谨慎修改
本段内容作为指引性介绍， 默认的线程属性可以满足绝大多数开发要求，只有及特殊情况可能修改属性
1.定义线程属性
2.初始化线程属性初始化后为默认属性
3.修改线程属性
pthread\_attr\_getstack(pthread\_attr\_t \* attr , void \*\* stntkaddr , size\_t \* statcksize)
pthread\_attr\_setstack(pthread\_attr\_t \* attr , void \*\* stntkaddr , size\_t \* statcksize)
如果要修改线程栈，需要自行申请栈空间 malloc
pthread\_attr\_getdetachstate(pthread\_attr\_t \* attr ,int \* detachstaet)
pthread\_attr\_setdetachstate(pthread\_attr\_t \* attr ,int \* detachstaet)
detachstate有两个关键字一个是分离态PTHREAD\_CREATE\_JOIINABLE，一个是回收态PTHREAD\_CREATE\_DETACHED
4.一定要用自定义属性创建线程
5.属性适用完毕后释放内存pthread\_attr\_destery()
``c
int main (void)
{
int detachstate;
void * stackaddr;
size_t stacksize;
pthread_attr_t attr;
pthread_attr_init(&attr);
//显示默认属性中的退出状态、栈地址、栈大小
pthread_attr_getdetachstate(&attr,&detachstate);
if(detachstate==PTHREAD_CREATE_JOINABLE)
printf("attr exit_status its JOIN\n");
else
printf("attr exit_status its DETA\n");
pthread_attr_destroy(&attr);
}
```
```c
void * thread_job(void * arg)
{
while(1)
sleep(1);
}

int main (void)
{
int detachstate;
void * stackaddr;
size_t stacksize;
pthread_attr_t attr;
pthread_attr_init(&attr);
//显示默认属性中的退出状态、栈地址、栈大小
pthread_attr_getdetachstate(&attr,&detachstate);
if(detachstate==PTHREAD_CREATE_JOINABLE)
printf("attr exit_status its JOIN\n");
else
printf("attr exit_status its DETA\n");
pthread_attr_getstack(&attr,&stackaddr,&stacksize);
printf("attr stack_info=%p,size=%d\n",stackaddr,stacksize);
//设置属性中退出状态，设置为分离，创建分离线程
pthread_t tid;
int err;
pthread_attr_setdetachstate(&attr,PTHREAD_CREATE_DETACHED);
pthread_create(&tid,&attr,thread_job ,NULL);
pthread_join(tid,NULL);
if((err=pthread_join(tid,NULL))>0)
{
printf("join failed:%s\n",strerror(err));
exit(0);
}
pthread_attr_destroy(&attr);
}
```
```c
void * thread_job(void * arg)
{
while(1)
sleep(1);
}

int main (void)
{
int detachstate;
void * stackaddr;
size_t stacksize;
pthread_attr_t attr;
pthread_attr_init(&attr);
//显示默认属性中的退出状态、栈地址、栈大小
pthread_attr_getdetachstate(&attr,&detachstate);
if(detachstate==PTHREAD_CREATE_JOINABLE)
printf("attr exit_status its JOIN\n");
else
printf("attr exit_status its DETA\n");
pthread_attr_getstack(&attr,&stackaddr,&stacksize);
printf("attr stack_info=%p,size=%d\n",stackaddr,(int)stacksize);
//设置属性中退出状态，设置为分离，创建分离线程
pthread_t tid;
int err;
pthread_attr_setdetachstate(&attr,PTHREAD_CREATE_DETACHED);
//pthread_create(&tid,&attr,thread_job ,NULL);
//pthread_join(tid,NULL);
//if((err=pthread_join(tid,NULL))>0)
//{
//printf("join failed:%s\n",strerror(err));
//exit(0);
//}
int flags=0;
stacksize=0x100000;//1M
while(1)
{
if((stackaddr=(void*)malloc(stacksize))==NULL)
{
perror("malloc thread stack failed");
exit(0);
}
pthread_attr_setstack(&attr,stackaddr,stacksize);
if((err=pthread_create(&tid,&attr,thread_job,NULL))>0)
{
printf("thread create failed:%s\n",strerror(err));
exit(0);
}
printf("thread number %d\n",++flags);
}
pthread_attr_destroy(&attr);
}
```
线程安全
访问互斥
多线程访问全局资源或静态资源，多线程访问文件数据,多线程适用共享数据引发异常
```c
int number;
void * thread_job(void * arg)
{
pthread_detach(pthread_self());
for(int i=0;i<5000;i++){
printf("pthread 0x%x  ++number %d\n",(unsigned int)pthread_self(),++number);
}
pthread_exit(NULL);
}

int main (void)
{
pthread_t tid;
pthread_create(&tid,NULL,thread_job,NULL);
pthread_create(&tid,NULL,thread_job,NULL);
while(1)
{
sleep(1);
}
return 0;
}
```
互斥锁
```c
pthread_mutex_lock();//上锁操作
pthread_mutex_unlock();//解锁操作
```
互斥锁避免多线程同时访问资源， 避免资源异常，结果异常
```c
pthread_mutex_t lock//互斥锁
pthread_mutex_init(&lock,NULL)//互斥锁初始化
pthread_mutex_destroy(&lock)//释放互斥锁
pthread_mutex_lock(&lock)//申请锁
pthread_mutex_trylock();//非阻塞申请，锁被占用不会阻塞，立即返回
pthread_mutex_unlock(&lock)//释放锁
```
加锁的位置问题。 可能改变线理执行流程
参考， 只有全局资源读写时需要上锁
```c
int number;
pthread_mutex_t lock;
void * thread_job(void * arg)
{
pthread_detach(pthread_self());
int tmp;
for(int i=0;i<5000;i++)
{
pthread_mutex_lock(&lock);
tmp=number;
printf("pthread 0x%x  ++number %d\n",(unsigned int)pthread_self(),++tmp);
number=tmp;
pthread_mutex_unlock(&lock);
}
pthread_exit(NULL);
}

int main (void)
{
pthread_t tid;
pthread_create(&tid,NULL,thread_job,NULL);
pthread_create(&tid,NULL,thread_job,NULL);
while(1)
{
sleep(1);
}
pthread_mutexattr_destroy(&lock);
return 0;
}
```
惊群问题， 多线程争抢资源， 因资源有限， 来抢到的线程付出了无意义的系仇开销
标记在某线程占用锁资源时自动分发
就近原则，某个线程释放了锁立即申请， 它还会占用锁
[![38.png](https://i.postimg.cc/d1HnJc6h/38.png)](https://postimg.cc/YGFQxVJ7)
读写锁
互斥锁不允许多个线程同时访问资源，资源的利用率较低，读写锁可以解决这个问题，它支持一个线程写资源，多个线程可以同时读资源提高资源利用率
读共享，写独占，读写互斥锁
```c
pthread_rwlock_t lock //读写锁
pthread_rwlock_init(&lock，NULL) //互斥锁初始化
pthread_rwlock_destroy(&lock) //程放互斥锁
pthread_rwlock_rdlock(&lock): //申请读锁
pthread_rwlock_wrlock(&lock): //申请写锁
pthread_rwlock_unlock(&lock): //释放锁
旋转锁/自旋锁
不会挂起等待锁， 一直重复请求，直到获取成功位置， 请求旋转锁的线程不会挂起， 一直处于运行态R
```c
int number;
pthread_rwlock_t lock;
void * thread_wr(void * arg)
{
while(1)
{
pthread_rwlock_wrlock(&lock);
printf("write thread 0x%x ++number = %d\n",(unsigned int)pthread_self(),++number);
pthread_rwlock_unlock(&lock);
usleep(100000);
}
}
void * thread_rd(void * arg)
{
while(1)
{
pthread_rwlock_rdlock(&lock);
printf("read thread 0x%x number=%d\n",(unsigned int)pthread_self(),number);
pthread_rwlock_unlock(&lock);
usleep(100000);
}
}
int main(void)
{
pthread_t tids[8];
pthread_rwlock_init(&lock,NULL);
int i;
for(i=0;1<3;i++)
{
pthread_create(&tids[i],NULL,thread_wr,NULL);
}
for(i;i<8;i++)
{
pthread_create(&tids[i],NULL,thread_rd,NULL);
}
while(i--)
pthread_join(tids[i],NULL);
pthread_rwlock_destroy(&lock);
exit(0);
}
```
文件读写锁
把写锁， n把读锁，读共享，写独占，读写互斥
结构体名：struct flock
//表示上锁方式，包含上读锁， 写锁和解锁，F_RDLCK F_WRLCK F_UNLCK
[![39.png](https://i.postimg.cc/VsTShxVZ/39.png)](https://postimg.cc/14G5njPD)
文件锁通过修改文件锁属性实现上锁和解锁效果
//上锁的绝对位置，SEEK_SET，SEEK_CUR SEEK_END 
//相对位置，是依据绝对位置描述的
//可以直行填写上锁长度， 如果传0则锁整个文件
//pid中存储当前占用文件锁的进程id
文件锁通过修改文件锁属性实现上锁和解锁效果，用户需要自定义锁结构体并赋值，而后对文件默认锁结构进行替换，实现文件锁操作
```c
fcntl(fd,F_GETLK,struct * lock);//将文件默认的锁结构体传出到lock变量中
fcntl(fd,F_SETLK,struct flock * newlock); //将自定义的newlock替换文件原有的结构体，实现上锁效果 F_SETLK是非阻塞上锁
F_SETLKW //阻寨上锁关键字，如果文件锁被占用，则会挂起等待
```
```c
A:
int main(void)
{
//判断文件锁属性，查看是否可以上锁
struct flock old;
int fd = open("pthread_test.c",O_RDWR);
fcntl(fd,F_GETLK,&old);
if(old.l_type == F_UNLCK)
{
printf("process A %d get flock successly .lock status its unlock.. \n",getpid());
struct flock new;
new.l_type = F_WRLCK;
new.l_whence = SEEK_SET;
new.l_start = 0;
new.l_len = 0;
fcntl(fd,F_SETLKW,&new);
printf("process A %d Set wrtie lock successly..\n" ,getpid());
sleep(10);
new.l_type=F_UNLCK;
fcntl(fd,F_SETLKW,&new);
printf("process A %d Set wrtie unlock\n" ,getpid());
}
else
printf("pthread test lock status is not unlock..\n");
return 0;
}

B:
int main(void)
{
//判断文件锁属性，查看是否可以上锁
struct flock old;
int fd = open("pthread_test.c",O_RDWR);
struct flock new;
new.l_type = F_WRLCK;
new.l_whence = SEEK_SET;
new.l_start = 0;
new.l_len = 0;
fcntl(fd,F_SETLKW,&new);
printf("process B %d Set wrtie lock successly..\n" ,getpid());
return 0;
}
```
死锁问题
锁资源有限，但多线程相互请求锁资源 导致线程永久阻塞， 这种现象成为死锁
[![40.png](https://i.postimg.cc/bwjpRs4T/40.png)](https://postimg.cc/D859vyvJ)
死锁发生的四个必要条件:
请求与保持条件: 某个线程在占用一把锁后还要请求新锁， 容易引发死锁问题
不可剥夺条件: 除了占用资源的线程外， 其他人无法解锁资源
互斥条件: 某个线程占用锁资源后，其他线程申请则挂起等待
环路等待条件: 每个线程都在等待相邻线程手中的资源， 这种成为等待环路死锁处理:
产生死锁后，杀死死锁线程，解除死锁，而后再创建(死锁频繁，
创建销毁线程开销较大)
死锁检测:
有向图检测
广度优先遍历算法
深度优先遍历算法
可以通过图遍历算法检测出，图中是否出现环路，如果是则已发生死锁，可以通过杀死线程发的方式杀死某个节点，解除死锁
死锁预防
暂学家只有两种工作模式， 思考和进食
思考不占用资源，进餐时每个哲学家先获取左手的筷子，再获取右手的筷子
死锁现象:
5名哲学家同时进餐，分别拿起左手的筷子，等待获取右手的筷子，产生死锁问题，永久挂起
礼貌策略:
当某个哲学家拿起左手的资源，发现无法获取右手的资源，它会放下左手资源，让其他人进餐
活锁问题，如果哲学家同时频繁触发礼貌机制，导致所有哲学家拿起放下餐具， 无法进食，饿死
高权级策略，选中一名哲学家提高权限，此哲学家要进餐时，向相邻哲学家发送通知，让其放下资源
高权策略， 由于优先级转换， 可能导致多数时间，只有超级哲学家在进餐
多线程情景下， 资源有限， 多线程合理的规避问题， 合理使用资源
服务者模式，银行家算法
银行家算法转资源都抽象为银行资产，每个用户借款银行进行借款风险评估，如果风险超出阈值，禁止放款
[![41.png](https://i.postimg.cc/rw3Wg6Sc/41.png)](https://postimg.cc/w157TGfb)
线程控制（条件变量）
条件变量技术实现线程的挂起和唤醒
为线程指定执行条件，按执行条件挂起唤醒控制线程
pthread\_cond \_tcd //条件变量类型 ， 线程可以挂起在条件变量中，也可以从中唤醒
pthread\_cond\_init(pthread\_cond\_t\* cd，NULL)://初始化条件变量
pthread\_cond\_destroy(pthread\_eond\_t \* cd); //销毁释放条件变母
pthread\_cond\_waitpthread\_cond\_t \* cd , pthread\_mutex\_t \* lock)
两次执行
线程第一次执行wait雨数，挂起钱程的同时解锁互斥锁





