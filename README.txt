# PenetrationTest
渗透方法实践论

灵活，变通，

目前研究的方向：
一、信息收集
   公开信息收集（来自于公开的库）
   目标网站信息收集（主动扫描与被动扫描）
   后渗透信息收集（目标系统本身及存放的文件各种敏感信息收集）
二、操作系统及服务漏洞扫描
   操作系统漏洞扫描（包括架设在其上的应用服务协议）
   CVE官网获取漏洞库去和目标系统做对比
三、操作系统及服务漏洞利用
    Metasploit 直接从Exploit-DB上下载exploit漏洞利用程序，得到反向连接或shell
四、web应用漏洞扫描

五、web应用漏洞利用

六、内网渗透
   域渗透
   arp是最后选择的内网渗透方案
   
七、痕迹清理
      若是Win系统，可利用Kali Linux中的Metasploit中的clearev的工具删除Log文件
      或者安装Windows日志清理工具Clearlogs:下载地址
      手工执行命令: del %WINDR%\* .log /a/s/q/f
      2.Linux系统
      删除/var/log下的文件即可: rm -f -r /var/log
      另外在bash shell中也保存了最后500条命令的记录，用more ~/.bash_history即可看到
         使用命令：export HISTSIZE=0 即可删除
         也有一个更快删除历史文件的方法：使用命令   shred -zu /root/.bash_history即可彻底清除所有的历史纪录文件并用空字符去覆盖文件。
