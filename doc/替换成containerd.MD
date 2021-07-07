


### 注意点
```
对KUBELET_EXTRA_ARGS修改
/etc/default/kubelet
KUBELET_EXTRA_ARGS="--container-runtime=remote --container-runtime-endpoint=unix:///run/containerd/containerd.sock"
```
### 错误处理

1.启动kubelet失败,kubeadm init解决，通过systemctl status kubelet.service查看kubelet状态。

### 查看kubelet日志
```
用journalctl查看日志非常管用
journalctl -u kube-scheduler
journalctl -xefu kubelet
journalctl -u kube-apiserver
journalctl -u kubelet |tail
journalctl -xe
```

### 参考文档

```
https://cloud.tencent.com/developer/article/1868092
https://blog.frognew.com/2021/04/relearning-container-02.html
https://blog.51cto.com/u_15127565/4325277
https://www.jianshu.com/p/344f2625bfea ## nerdctl 运行报错，安装cni插件解决
```