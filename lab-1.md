实验中遇到的问题
====
### 问题1：华为云连接timeout  

<img width="415" height="56" alt="image" src="https://github.com/user-attachments/assets/848a3b7b-a8ca-48ac-bed9-a9fed4bc4ce3" />  

原因&解决办法：华为云上没有设置打开对应端口，配置安全组规则，在入方向规则处勾选“一键放通常用端口”。    

方法来源：询问豆包  

<img width="477" height="100" alt="image" src="https://github.com/user-attachments/assets/1ffb4b85-a29a-4fd2-869f-b548727ef0d9" />  

结果：成功连接  

<img width="386" height="245" alt="image" src="https://github.com/user-attachments/assets/f45bb396-f4f9-4830-85ed-cc6709eced12" />  

### 问题2：编译test1-1.c时报错  

<img width="415" height="42" alt="image" src="https://github.com/user-attachments/assets/239e4d91-57b3-45d7-931e-3d10667b5131" />  

原因&解决办法：wait函数的头文件没有声明，在文件开头添加"#include<sys/wait.h>"。  

方法来源：询问豆包  

结果：成功编译  



