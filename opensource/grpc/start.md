# grpc

## 要求

cmake >= 3.13
gcc >= 7.5.0

## 版本

grpc V1.38.1

## 下载源码

``` bash
git clone -b V1.38.1 https://github.com/grpc/grpc.git --depth 1
cd grpc
git submodule update --init
```

## 编译

参考文档：<https://github.com/grpc/grpc/blob/master/BUILDING.md>

``` bash
cd grpc
mkdir -p cmake/build
cd cmake/build
cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON -DgRPC_INSTALL=ON ../..
```

gRPC_USE_PROTO_LITE=ON 表示使用lite版本protobuf

## FAQ

1. ZLIB相关错误

   ``` text
   gRPC_ZLIB_PROVIDER is "module" but ZLIB_ROOT_DIR is wrong
   ```

   - 手动到third_party/zlib目录拉取代码
      `git checkout -f`

2. 编译demo helloworld时提示absl文件找不到
   - 原因时absl头文件没有安装上，进入到third_party/abseil-cpp

     ``` bash
     mkdir cmake/build -p
     cd cmake/build
     cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON ../..
     cmake --build . -- -j
     sudo make install
     sudo ldconfig
     ```
