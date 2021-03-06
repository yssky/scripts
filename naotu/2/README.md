### 黑产运营流程

#### 入侵者要做什么？

控制肉鸡、构建僵尸网络、控制重要主机、批量入侵主机、编写释放蠕虫、网站挂马、入侵游戏服务器、植入广告、植入暗链、侵占计算资源、发送垃圾邮件、挖掘系统漏洞、入侵路由器等

#### 获取哪些信息？

窃取主机信息、窃取源代码、窃取个人隐私、控制数据库、盗窃银行账号、盗窃证券账号、盗窃信用卡号、盗窃虚拟货币、盗窃游戏账号等

#### 出售哪些信息？

出售个人信息、出售个人隐私、出售主机信息、出售虚拟货币、出售控制权限、出售游戏账号、出售路由器后门、出售系统漏洞、出售关键技术/设计资料/财务数据、出售漏洞等

#### 出售对象是谁？

敌对势力、情报买家、反动势力、竞争对手、中间批发商、传统销售商、非法勒索者、后门编写者、电信诈骗集团、技术爱好者、游戏销售平台、虚拟货币销售平台、银行卡复制者、电商/证券、黄色网站经营者、网站经营者等

#### 达到的目的是什么？

敌对势力政治献金、宣传发动言论、执行破坏活动、收取佣金、洗钱、执行拒绝服务、提升搜索排名、诈骗/勒索/盗刷等一系列目的获得金钱。

---

### 信息系统生命周期安全

#### 需求设计

提出安全需求点

**防护措施**

验证码的强度、密码的复杂度、通讯安全（https）等

**数据保护**

敏感信息分类、分级保护等

#### 系统开发

**开发设计**

*常见高危漏洞处理办法：*SQL注入、XSS跨站攻击（包含盲打）、弱口令攻击、任意文件下载、数据导入、文件上传、逻辑漏洞、命令执行、遍历等

*接口交互安全：*内部互联、外部互联

*第三方编辑器：*FckEditor、ewebediter等

*错误数据处理*

**编码**

*验证具体函数应用场景*

1 SQL注入查看变量传入前是否有相应的过滤

2 XSS脚本要查看变量输入时是否编码

3 其他问题验证

*引入OWASP ESAPI解决OWASP TOP10安全问题*

#### 测试

**SIT测试（开发过程迭代测试）**

*黑盒测试：*SQL注入、XSS跨站（包括盲打）、弱口令攻击、配置文件泄露（类似于.svn、.rar文件、.history等）、任意文件下载、数据导入、文件上传、逻辑漏洞、命令执行、钓鱼攻击、社会工程学、系统接口测试、遍历、导出安全测试报告等

*白盒测试：*工具自动代码审计、人工代码审计

*手动人工安全测试*

**UAT测试（验收测试）**

回归测试SIT测试所有问题暴露的安全问题

**测试类型**

文档测试、标准符合性测试、数据及数据库完整性测试、用户界面测试、功能测试、业务逻辑测试、性能测试、安全性测试、兼容性测试、配置测试、故障转移及恢复测试、易用性测试、可靠性测试、本地化及国际化测试、其他类型测试

#### 系统上线

**操作系统**

*内核优化：*syn防护设置、并发连接数设置、文件并发

*系统环境检查：*操作系统补丁、防病毒软件

*系统最小化：*系统服务、端口、应用、文件权限、用户账户权限、ip访问策略

**web容器**

*Apache：*版本漏洞、性能优化、安全优化

*Tomcat*

*Weblogic*

*Nginx*

等

**网络环境**

*安全设备：*防火墙、IPS、IDS、堡垒机等

*安全域划分：*外网区（前端缓存）、内网区（数据缓存区、数据库区、办公区）、管理网（互联网管理-、企业内部管理）

*安全策略：*权限最小化原则

#### 安全运维

**周期安全评估、模拟渗透测试**

渗透、审计工具（APPscan、burpsuite等）、审计流程、步骤

**安全审计**

*对象：*服务器、网络设备、安全设备、数据库周期安全审计

*项目：*有效账户控制、弱口令审计、权限审计、ACL访问审计、行为日志审计、设备自身配置安全审计

**安全相关规范流程**

网络端口开放策略规范、漏洞修补流程、安全事件处理流程、网站应用上线安全测试规范/流程

**安全交流，分享，培训**

部门内部分享/交流、跨部门培训（运维/QA/DEV）、面向企业的安全习惯/意识/TIPS

**IDC相关的制度/规范标准**

生产网络服务器/网络设备上线，下线流程、IDC边界端口/内部互访的ACL开放审批流程、服务器/网络设备账户，权限，行为审批流程、系统，网络，安全设备安全加固标准、重要数据的存储。传输加密规范，流程

---

### 数据库安全

#### 数据库安全风险分析及对策

**数据安全风险分析**

数据被篡改、数据被盗取、用户身份被伪造

**典型数据安全攻击方式**

sql注入、网络窃听、未经授权的服务访问、密码破解、

**数据库管理要点**

数据库安全管理员独立性原则、最小权限原则、账户安全原则、安全审计原则、数据库安全防护原则

---

### 信息安全

#### 内部环境安全

**系统安全**

邮件系统、OA系统、域控服务器、DNS服务器、FTP服务器、文件服务器、邮件服务器、数据库服务器、堡垒机、漏洞扫描、补丁升级、路由器、交换机、认证服务器、代理服务器、代码服务器等

**网络安全**

ARP防护、入侵检测、区域划分、无线安全、准入技术、流量分析安全**

病毒扫描、木马，蠕虫扫描、主机IDS防护、补丁更新

**物理安全**

机房门禁、保安、监控、报警

#### 外部环境安全

**应用安全**

代码审计、注入扫描、xss扫描、webshell扫描、功能测试、waf部署、代码管理、编码规范

**系统安全**

漏洞扫描、端口扫描、补丁更新、弱口令检测、权限账户审计、配置管理、日志审计、异常行为检测、病毒木马后门检测

**网络安全**

ARP防护、入侵检测、流量分析、漏洞扫描、配置管理、安全区域划分、防DDOS

**数据库安全**

重要的信息加密、操作审计、日志审计、角色控制、数据库备份、补丁更新

**操作安全**

配置标准化、变更控制、堡垒机应用、操作账户安全、统一权限管理、日志管理

**物理安全**

#### 业务安全

**身份认证安全**

暴力破解、cookie&session、加密测试

**业务一致性安全**

手机号篡改、邮箱和用户名更改、订单ID更改、商品编号更改、用户ID篡改

**业务数据篡改**

金额数据篡改、商品数量篡改、最大数限额突破、本地js参数修改

**用户输入合规性**

注入、xss、fuzz

**密码找回漏洞**

*用户凭证暴力破解*

*返回凭证：*url返回验证码及token、密码找回凭证在页面中、返回短信验证码

*邮箱弱token：*时间戳的md5、用户名、服务器时间

*用户凭证有效性：*短信验证码、邮箱token、重置密码token

*重新绑定：*手机绑定、邮箱绑定

*服务器验证：*最终提交步骤、服务器验证可控内容、服务器验证逻辑为空

*用户身份验证：*帐号与手机号码的绑定、帐号与邮箱帐号的绑定

*找回步骤：*跳过验证步骤、找回方式，直接发哦设置新密码页面

*本地验证：*在本地验证服务器的返回信息，确定是否执行重置密码、但是其返回信息是可控的内容或者可以得到内容、发送短信等验证信息的动作在本地进行，可以通过修改返回包进行控制

*注入：*在找回密码处存在注入漏洞

*token生成：*token生成可控

*注册覆盖：*注册重复的用户名

*session覆盖*

**验证码突破**

暴力破解、次数突破、回显测试、绕过测试

**业务授权安全**

未授权访问、越权测试

**业务流程乱序**

顺序执行缺陷

**业务接口调用**

恶意注册、短信炸弹、内容编辑

**时效绕过测试**

时间刷新缺陷、时间范围测试

#### 安全事件

**事前**

信息收集、标准化、基础数据建立、风险评估、端口及漏洞扫描、病毒，木马，网马，webshell扫描、渗透测试、补丁更新、配置管理、安全域划分、事件响应团队及处理流程、日志收集、日志分析、安全预警体系、安全检测体系、安全防御体系、安全培训、账户登录及权限管理、跨部门交流

**事中**

管理路径分析、响应机制、防御及影响评估、流量，行为，攻击分析

**事后**

日志分析、调查取证、经验总结、加固

### 总结

今天分享的几个脑图还是关于整个企业信息安全相关技术，有兴趣看原图的可以点阅读原文查看。

