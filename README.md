> hcmd 是一个简单方便的cmd 工具,可以在windows和linux下运行

## 下载地址

```
https://github.com/seakingii/hcmd/releases
```

## 主要功能 

### 下载大文件
```
hcmd download 
```
工具会启动5个线程去分段下载文件

### 打印硬件信息

```
hcmd hardware
```

### 静态文件服务器

```
hcmd fileserver
```

立即起一个WEB服务,将指定的目录里的文件以HTTP方式提供访问

### tcp代理

```
hcmd tcpproxy
```

起一个tcp代理服务



### 字符串hash计算

```
hcmd hash_string  要计算的字符串 --type 算法类型
```

算法类型有:

1. md4
2. md5
3. sha1
4. sha256
5. sha512
6. rc4
7. ripemd160
8. sha224
9. sha384


### 字符串编码 

```
hcmd encode_string 要编码的字符串 --type 编码算法
```

编码算法有:

1. base16
2. base32
3. base58
4. base62
5. base64
6. base64url
7. base85
8. base91
9. base100
10. morse
11. safeurl


### 字符串解码 

```
hcmd decode_string 要解码的字符串 --type 解码算法
```

解码算法有:

1. base16
2. base32
3. base58
4. base62
5. base64
6. base64url
7. base85
8. base91
9. base100
10. morse
11. safeurl


### hash文件 计算文件的HASH值 

```
hcmd hash_file 文件 --type HASH算法
```

或者 显示进度条

```
hcmd hash_file 文件 --type HASH算法 --progress true
```

HASH算法有:

1. md5
2. sha1
3. sha256
4. sha512



### 产生唯一ID字符串

```
hcmd id
```


### 列出本地的IP地址

所有IP

```
hcmd ip
```

IPV4
```
hcmd ipv4
```

IPV6

```
hcmd ipv6
```


### 列出本机所有进程

```
hcmd processes
```


### 显示本机的磁盘使用情况 

```
hcmd diskusage 
```

或者简单一点的

```
hcmd du
```

### 监控本机的资源占用监控

```
hcmd monitor
```

### 监控本机的CPU资源

```
hcmd monitor_cpu
```

### 监控本机的进程

```
hcmd monitor_proc
```

或者只监控一个进程 

```
hcmd monitor_proc -p 进程ID
```

### 监控本机的容器


```
hcmd monitor_container
```

### 创建一个 systemd 服务

```
hcmd systemd
```

### 创建一个 web terminal 服务

默认端口 2000

```
hcmd web_terminal
```

指定端口

```
hcmd web_terminal --port 1234
```



客户端可以用网页访问此模拟终端


> 后续将陆续更新添加新的功能



