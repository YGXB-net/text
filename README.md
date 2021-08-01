# text

# 加速镜像配置

访问[容器镜像服务 (aliyun.com)](https://cr.console.aliyun.com/cn-hangzhou/instances/mirrors)

![image-20210504170010392](image-20210504170010392.png)

### Ubuntu、Debian、CentOS

对于使用 systemd 的系统，请在 /etc/docker/daemon.json 中写入如下内容（如果文件不存在请新建该文件）：

```shell
{
  "registry-mirrors": ["加速地址"]
}
```



```shell
sudo systemctl daemon-reload
sudo systemctl restart docker
```

