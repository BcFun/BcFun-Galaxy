# 如何同步语雀文档至github
同步代码：  
[https://github.com/BcFun/galaxy-yuque-sync](https://github.com/BcFun/galaxy-yuque-sync)  
目标库  
[https://github.com/BcFun/BcFun-Galaxy](https://github.com/BcFun/BcFun-Galaxy)

## 环境配置

由于保密性，所以设置在[Secrets](https://docs.github.com/cn/actions/reference/encrypted-secrets)中

- YUQUE_USER_TOKEN=xxx 语雀开发者 token
- YUQUE_LOGIN=xxx 语雀账号域名
- YUQUE_REPOS=xxx 语雀知识库名称，字符串类型，,分割
- GH_TOKEN=xxx github token
- GH_LOGIN=xxx github 账号域名
- GH_REPO=xxx github 项目名称

​

比如

```
YUQUE_USER_TOKEN=xxx
YUQUE_LOGIN=igsrxe
YUQUE_REPOS=we3pfy
GH_TOKEN=xxx
GH_LOGIN=BcFun
GH_REPO=BcFun-Galaxy
```

​

## 其他

利用 github action，通过 cron 表达式定时执行，目前每周三同步一次。  
[https://github.com/BcFun/galaxy-yuque-sync/blob/master/.github/workflows/main.yml](https://github.com/BcFun/galaxy-yuque-sync/blob/master/.github/workflows/main.yml)  
缺点  
目前是增量同步，不是全量同步  
​

<br>
  
> 语雀地址 https://www.yuque.com/igsrxe/we3pfy/hvwtrm