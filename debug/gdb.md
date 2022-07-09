# gdb

## 常用指令

### 查看结构体大小

objdump --dwarf=info xxx
structres there as *DW_TAG_structure_type* and *DW_AT_byte_size* attribute is equivalent to sizeof.

### 查看地址内容

x/9xg addr

### 查询对应的类型信息

info types xxx

ptype xxx

### 查询符号信息

info symbol xxx