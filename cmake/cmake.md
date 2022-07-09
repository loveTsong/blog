# cmake

## 判断是否是子工程

```cmake
if(NOT PROJECT_NAME)
    project(xxx)
    cmake_minimum_required(VERSION x.y)
endif()
```

```cmake
if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_CURRENT_SOURCE_DIR})
    project(xxx)
    cmake_minimum_required(VERSION x.y)
endif()
```

## 数组参数传入宏

注意需要加双引号，否则会展开为多个参数。如：func("${listVar}")

## 宏的返回值处理

```cmake
macro(func, result)
    set(${result} xxx)
endmacro()
```

## 获取子目录

file(GLOB subDirListVar RELATIVE ${dir}/[pattern])

## 字符串匹配

string(FIND ${target} ${findStr} resultPosVar)
if(NOT (${resltPosVar} EQUAL -1))
endif()