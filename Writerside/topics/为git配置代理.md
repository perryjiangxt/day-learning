# 为git配置代理

## 读取git配置信息

查看git全局配置
```Bash
git config --global --list
```
查看git当前项目配置
```Bash
git config --list
```

git配置文件位置

全局文件为 ～/.gitconfig
git仓库下为 projectFolder/.git/config

## 配置代理
修改git配置可以通过命令行或修改配置文件

### 命令行
```Bash
git config --global http.proxy  http://127.0.0.1:10080
git config --global https.proxy  http://127.0.0.1:10080
git config --global core.gitproxy  http://127.0.0.1:10080
```

### 修改配置文件
修改配置文件，在配置文件最后追加。如果已存在则修改。
```Bash
[http]
    proxy = http://127.0.0.1:10080
[https]
    proxy = http://127.0.0.1:10080
[core]
    gitproxy = http://127.0.0.1:10080
```

<seealso>
   <category ref="external">
       <a href="https://blog.csdn.net/zwhfyy/article/details/130739079">设置代理和取消代理</a>
   </category>
</seealso>
