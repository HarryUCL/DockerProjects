1. WIndterm中写入compose.yaml
	命令行输入：vim compose.yaml
	点击i进入插入模式，粘贴compose.yaml全文。退出时先ESC键后输入:wq
2. 创建compose.yaml安排的卷,网络和镜像
	命令行输入docker compose -f compose.yaml up -d
	返回如下，即为创建成功：
[+] Running 5/5
 ✔ Network root_blog         Created                                                                                                                 0.0s 
 ✔ Volume "root_wordpress"   Created                                                                                                                 0.0s 
 ✔ Volume "root_mysql-data"  Created                                                                                                                 0.0s 
 ✔ Container mysql           Started                                                                                                                 0.3s 
 ✔ Container wordpress       Started  
3. 下线compose.yaml中约定的服务：
	命令行输入docker compose -f compose.yaml down
	返回如下：
[+] Running 3/2
 ✔ Container wordpress  Removed                                                                                                                      1.1s 
 ✔ Container mysql      Removed                                                                                                                      0.6s 
 ✔ Network root_blog    Removed 
