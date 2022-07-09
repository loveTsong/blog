# docker

## 容器中使用systemctl

docker run --restart=always --net=host -d -it -name xxx -w "dir" --privileged=true image /sbin/init