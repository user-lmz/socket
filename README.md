配置过程
	在unpv13e/libfree下找到inet_ntop.c文件把#include <arpa/inet.h>注释掉
	![image](https://user-images.githubusercontent.com/52618022/138024548-fb61d1e0-d4f6-4c9a-add3-eb65360aa7a8.png)
    然后在unpv13e文件夹中make成功生成libunp.a文件
    
    将生成的libunp.a文件复制到usr/lib文件夹中，并且将unpv13e下的config.h和修改后的unpv13e/lib中的unp.h复制到usr/include文件夹中
	首先将unp.h中的#include "…/config.h"修改为#include “config.h” ，因为unp.h和config.h都放入usr/include中
	执行命令：（都是在unpv13e文件夹中）
		sudo cp libunp.a /usr/lib
		sudo cp lib/unp.h /usr/include   
		sudo cp config.h /usr/include
	
