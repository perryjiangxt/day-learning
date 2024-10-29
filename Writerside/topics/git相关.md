# git相关

### 用户名和密码

```
git config --global user.name "perryjiang7_v"
git config --global user.email "jiangpeng7_v@didiglobal.com"

git config  user.name "perryjiang"
git config  user.email "perryjiangxt@gmail.com"
```

### 配置和取消配置代理

```
#移除设置
git config --global --unset http.proxy
git config --global --unset https.proxy
#重新设置
git config --global https.proxy http://127.0.0.1:10080
git config --global https.proxy https://127.0.0.1:10080

git config  https.proxy http://127.0.0.1:10080
git config  https.proxy https://127.0.0.1:10080

```