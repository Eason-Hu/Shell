# 编写可靠的Shell脚本
## 指定bash
在Shell第一行指定bash，#!后面应该跟什么呢？，推荐使用这两种写法。
```shell
#!/usr/bin/env bash
```
或者
```shell
#!/usr/bash
```
前者通过env添加一个中间层，让env在$PATH中搜索bash；后者是官方约定俗成的bash位置。
## set -e和set -x
