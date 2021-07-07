## 设置root用户登录
```
sudo -s
vi /etc/ssh/sshd_config
PermitRootLogin yes
PasswordAuthentication yes
service sshd restart
passwd root
vagrant reload
vagrant ssh-config
ssh root@127.0.0.1 -p 2222
```
## 安装golang

```
安装golang 1.17.8：
wget https://studygolang.com/dl/golang/go1.17.8.linux-amd64.tar.gz
tar -zxvf go1.17.8.linux-amd64.tar.gz
mv go /usr/local/
vi /etc/profile
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
# 启用 Go Modules 功能~~
export GO111MODULE=on
# 配置 GOPROXY 环境变量
export GOPROXY=https://goproxy.cn,direct
source /etc/profile
go

```
