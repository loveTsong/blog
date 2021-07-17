# grpc

## 要求
cmake >= 3.13
gcc >= 7.5.0

## 下载源码
``` bash
git clone -b XXX https://github.com/grpc/grpc.git --depth 1
cd grpc
git submodule update --init
```

## 编译
参考文档：https://github.com/grpc/grpc/blob/master/BUILDING.md
``` bash
cd grpc
mkdir -p cmake/build
cd cmake/build
cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON -DgrpcInstall
```

## FAQ
1. ZLIB相关错误
   ```
   gRPC_ZLIB_PROVIDER is "module" but ZLIB_ROOT_DIR is wrong
   ```
   - 手动到third_party/zlib目录拉取代码
      `git checkout -f`

