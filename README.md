## fnOS

fnOS 下载地址：https://raw.githubusercontent.com/FNOSP/fnOS/refs/heads/main/fnOS.json

获取最新版本的 fnOS 镜像下载地址：
```shell
# E.g. 获取 fnOS-x86_64 最新版本的下载地址
curl -skL "https://raw.githubusercontent.com/FNOSP/fnOS/refs/heads/main/fnOS.json" \
| jq -r '[.[] | select(.name=="fnOS-x86_64")] | sort_by((.version | split(".") | map(tonumber)), .version) | last | .url'
```
