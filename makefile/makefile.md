# makefile

## 批量设置目标和增加目标依赖

```makefile

DIRS:=1 2
DIRS += 3
all: $(DIRS)
    @echo "$($DIRS)"

.PHONY:all

$(DIRS): %:%.dep
    @echo "$@:$^"

%.dep:
    @echo "default dep $@"

1.dep: 2
    @echo "1 dep $^"
```