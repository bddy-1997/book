### 所需工具

1. VPS 一台重置好主流的操作系统 （CentOS 7+、Ubuntu 16+、Debian 8+）
2. 域名一个，做好相关的解析，若需要套用 CDN，请托管域名到 cloudflare
3. FinalShell工具

### 全部链接

[finalshell远程连接工具](http://www.hostbuf.com/t/988.html)

[josthost服务器官网](https://justhost.ru/services/vps/?ref=21956)

[Namesilo域名](https://www.namesilo.com)

[Cloudflare CDN](https://dash.cloudflare.com/login)

[x-ui作者GitHub](https://github.com/vaxilu/x-ui)

[clash for 安卓](https://github.com/Kr328/ClashForAndroid/releases/tag/v2.5.4)

[qv2ray](https://github.com/ZZQ12325-GitHub/Qv2ray)

[xray](https://github.com/XTLS/Xray-core)

#### 更新及安装组件

```plain
apt update -y          # Debian/Ubuntu 命令
apt install -y curl    #Debian/Ubuntu 命令
apt install -y socat    #Debian/Ubuntu 命令
yum update -y          #CentOS 命令
yum install -y curl    #CentOS 命令
yum install -y socat    #CentOS 命令
```

#### 安装 Acme 脚本

```plain
curl https://get.acme.sh | sh
```

#### 80 端口空闲的证书申请方式

```plain
~/.acme.sh/acme.sh --register-account -m xxxx@xxxx.com   #记得更换邮箱
~/.acme.sh/acme.sh  --issue -d mydomain.com   --standalone   #记得更换为已经解析好的域名
```

#### 安装证书到指定文件夹

```plain
~/.acme.sh/acme.sh --installcert -d mydomain.com --key-file /root/private.key --fullchain-file /root/cert.crt   #记得更换域名
```


 

### 安装 & 升级 X-ui 面板

```plain
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
```

