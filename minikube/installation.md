# 安装Minikube

## Error sync pod
因为GFW的问题，拉取gcr.io/google_containers/pause-amd64:3.0镜像失败导致。
minikube ssh systemctl status localkube
可以看到日志信息

解决办法：
eval $(minikube docker-env)
docker pull registry.cn-hangzhou.aliyuncs.com/google-containers/pause-amd64:3.0
docker tag registry.cn-hangzhou.aliyuncs.com/google-containers/pause-amd64:3.0 gcr.io/google_containers/pause-amd64:3.0

