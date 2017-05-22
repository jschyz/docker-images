# Robot
这是微信自动回复机器人，基于[itchat](http://itchat.readthedocs.io/zh/latest/#_3)

### Usage

``` bash
$ docker build -t robot .
$ docker run -it robot
```

```
# 如部分的linux系统，块字符的宽度为一个字符（正常应为两字符），故赋值为2
itchat.auto_login(enableCmdQR=2)
```

详见: [itchat文档](http://itchat.readthedocs.io/zh/latest/)
