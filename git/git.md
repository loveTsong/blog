# git

## 常用设置

### 代理

```git
[http]
    sslverify=false
[http "https://github.com"]
    proxy=xxx
```

### 开启长路径

windows下gitbash使用

```git
[core]
    longpaths=true
```

### 自动转换unix/dos格式

windows下gitbash使用

```git
[core]
    autocrlf=input
```

### 别名

```git
[alias]
    s = status
    pr = pull --rebase
    lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```
