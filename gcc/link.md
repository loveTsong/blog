# 链接选项

## no-as-needed

-Wl,--no-as-needed 用来链接没有直接符号依赖的so,否则链接器不会链接没有使用到符号的库

## as-needed

和上述相反

## export-dynamic

-Wl,--export-dynamic
导出executable中的符号，默认是隐藏不导出的

## rpath-link=xxx

-Wl,rpath-link=xxx 设置链接库查找目录，依赖的依赖链接时也会寻找这些目录

## L{dir}

-L{dir} 链接查找目录，只针对显示配置的链接查找

## Bsymbolic

-Bsymboloc

## whole-archive

--whole-archive 链接静态库的所有符号，否则只链接使用到的符号，这是默认的行为

## 动态库加载

linux dlopen时使用local方式打开动态库时，其依赖的动态库的对外符号会加载到进程空间中全局可见