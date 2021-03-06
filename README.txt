
WEB安全分为四大模块：
  一、操作系统安全（常见企业级操作系统为Linux：CentOS）
     这部分安全规范 已归纳到GitHub：https://github.com/jidongdeatao/LinuxSafty
     
     这部分安全检测已有自动化脚本：
     https://github.com/jidongdeatao/LinuxTest/tree/master/NewVerson/SecurityTest/TestCase/systemSafe
        检查功能项包括：
        1.所有非root用户的文件权限：
        2.检查系统中不能安装调试工具：make|gcc|gcc-c++|cpp|gdb|binutils|glibc_devel|flex|tcpdump|mirror|glibc-devel|dexdump|toolbox|Netcat|Wireshark|ethereal
        3.检查系统中的无属主文件
        4.检查进程越权，产品进程是否用root账号启动
        5.检查进程中的敏感信息，关键字："pass|password|passwd|pswd|mima|key|pwd|PINNUMBER|secret|X-Auth-Token|Authorization|sessionID|token|email"
        6.检查进程中是否不允许使用的服务："bootps|pure-ftpd|pppoe|sendmail|isdn|zebra|cupsd|cups-config-daemon|hplip|hpiod|hpssd|bluetooth|hcid|hidd|sdpd|dund|pand|rsh|telnet"
        7.检查系统中是否含有不需要的账号
        8.检查系统账号的的密码加密安全（比如不能用Base64加密）
        9.运行数据库进程的帐号权限应该遵循最小权限原则，要使用操作系统的非管理员权限帐号来运行数据库
        10.检查是否安装了不安全的服务
        
     Linux sudo越权自动化脚本：
     sudo安全配置规范-对于sudo是否存在越权问题的排查可以使用自动化工具进行排查
    https://github.com/jidongdeatao/LinuxTest/blob/master/NewVerson/SecurityTest/TestCase/SudoersSafe/TestCase_SudoerSafe.py

     
  二、数据库安全（常见企业数据库为MySQL、Redis）
     这部分安全规范 已归纳到GitHub：https://github.com/jidongdeatao/Database/tree/master/DatabaseSafty
     
     MySQL安全检测已有自动化脚本：
     
  三、Docker容器安全
  
  
  四、WEB应用安全
    1.浏览器安全策略
      同源策略
      
    2.常见的WEB漏洞：
      XSS（Cross Site Script，跨站脚本攻击）
      Cross Site Request Forgery (CSRF， 跨站请求伪造)
      Session hijacking attack（Session 挟持）
      File inclusion vulnerability（文件包含漏洞）
      file upload attack（文件上传攻击）
      Weak Password Vulnerability（弱密码暴力破解）
      webshell（web 后门攻击）
      SQL Injection（SQL 注入）
      Distributed Denial of Service （DDoS， 分布式拒绝服务）
      XXE
      SSRF
      业务逻辑漏洞：
        1）密码重置漏洞
        2）认证：（Cookie与Session、Outh2.0）
        3）访问权限控制：（水平权限管理（基于数据的访问控制）、垂直权限管理（基于角色的访问控制）、RBAC模型）
      
  WEB相关安全漏洞整理：
    详见WEB-VulnerabilityDB
      
      
  常用的渗透方案：
  1.对网站进行侦查：操作系统、端口、应用服务架构
  2.漏洞扫描器：比对已有对漏洞库
  3.使用客户端代理测试安全性
  4.针对特定的服务器漏洞攻击：DOS-暴力破解-SQL注入
  5.使用网站后门维持访问
      
      

添加到WEBSecurity
一、业务逻辑漏洞（Logic error vulnerability）
定义：由于程序逻辑不严谨导致
特性：非常隐蔽，一般出现在功能（业务流程上），这是漏洞扫描工具无法识别的
常见分类：1.密码重置问题
                   2.cookies验证问题
                   3.越权操作问题

二、上传漏洞
利用put,move等http请求方法
本地图片
三、密码暴力破解
引用Security Tools工具
本地保存图片暴力破解分为c/s 与b/s
四、命令执行漏洞
本地图片
五、文件包含漏洞
本地图片

利用搜索引擎搜索信息添加到GOOGLE Hacking中
已保存到本地图片
     
