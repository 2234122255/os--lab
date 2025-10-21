实验中遇到的问题
====
## 问题1：华为云连接timeout  

<img width="415" height="56" alt="image" src="https://github.com/user-attachments/assets/848a3b7b-a8ca-48ac-bed9-a9fed4bc4ce3" />  

原因&解决办法：华为云上没有设置打开对应端口，配置安全组规则，在入方向规则处勾选“一键放通常用端口”。    

方法来源：询问豆包  

<img width="477" height="100" alt="image" src="https://github.com/user-attachments/assets/1ffb4b85-a29a-4fd2-869f-b548727ef0d9" />  

结果：成功连接  

<img width="386" height="245" alt="image" src="https://github.com/user-attachments/assets/f45bb396-f4f9-4830-85ed-cc6709eced12" />  

## 问题2：编译test1-1.c时报错  

<img width="415" height="42" alt="image" src="https://github.com/user-attachments/assets/239e4d91-57b3-45d7-931e-3d10667b5131" />  

原因&解决办法：wait函数的头文件没有声明，在文件开头添加`#include<sys/wait.h>`。  

方法来源：询问豆包  

结果：成功编译  

## 问题3：编译test2-1.c时报错  

<img width="416" height="79" alt="image" src="https://github.com/user-attachments/assets/d780b5a8-fa64-45cd-a374-e8a5a4acad7e" />  

原因&解决办法：在编译时没有链接到 pthread 库，修改编译命令为：`gcc test2-1.c -o tets2-1 -lpthread`。  

方法来源：询问豆包。  

结果：成功编译  

## 问题4：编译test2-3.c时报错  

<img width="415" height="195" alt="image" src="https://github.com/user-attachments/assets/fac7c8b4-6487-488a-8d00-5a826a2f8236" />  

原因&解决办法：pid 和 pid1 需声明为全局变量，否则子线程函数 pt1、pt2 无法访问（局部变量仅在声明的函数内有效）。

方法来源：询问豆包。  

结果：成功编译  

## 问题5：编译test3-1.c时报错  

<img width="455" height="132" alt="image" src="https://github.com/user-attachments/assets/c70ae1e8-9457-479e-ae0f-8f5d1dd8f28a" />  

原因&解决办法：①函数签名不匹配：pthread_create期待的函数类型是`void*(*）（void*)`,但我的add和sub函数的参数是`spinlock_t*`类型，需修改add、sub函数的参数为`void*`类型，并在函数内部进行强制类型转换；②编译时未链接到pthread库，应修改编译命令为：`gcc test3-1.c -o tets3-1 -lpthread`。  


方法来源：询问豆包。  

结果：成功编译  








