![](https://gitee.com/im0o/photobed/raw/master/img/20200406173358.png)

--------

# VPoints

一款可自定义多属性的金币兑换点券通道

## 插件功能

- 支持玩家使用指令将Vault经济的金钱转化为PlayerPoints金融
- 可基于权限节点给予玩家基础兑换次数上限
- 可自定义兑换通道（例：1000游戏币兑换1点券为一个通道）

## 指令＆权限

玩家指令（权限节点：vpoints.use）

[-] /vpoint help - 查看帮助

[-] /vpoint shop|s - 列出所有兑换通道

[-] /vpoint buy <序号> - 进行<序号>通道的兑换

管理员指令（权限节点：vpoints.admin）

[-] /vpoint add <玩家> <数量> - 增加玩家兑换次数的最大上限

[-] /vpoint rem <玩家> <数量> - 减少玩家兑换次数的最大上限

[-] /vpoint see <玩家> - 查看玩家兑换次数的最大上限与本日次数

[-] 基础兑换次数无法减少 玩家自拥有的最大兑换次数不能小于0

[-] /vpoint reload - 重载插件

[-] /vpoint reloadplayers - 直接更新所有玩家的次数(慎重使用)

## 配置文件

```yaml
#VPoints配置文件
#拥有某个权限节点的玩家基础的最大次数
#计算方式为:(拥有的节点转化为次数的和)+玩家额外拥有的次数
dtimes:
- vpoints.default:3
- vpoints.vip:6
#汇率设定
#可以理解为开放兑换的通道
#需要的vault数量:可兑换的points数量
#左边的数字不能重复 右边随意
rates:
- 100-1
- 1000-10
- 5000-51
```

## 游戏截图

![](https://gitee.com/im0o/photobed/raw/master/img/20200406174638.png)

![](https://gitee.com/im0o/photobed/raw/master/img/20200406174639.jpg)

![](https://gitee.com/im0o/photobed/raw/master/img/20200406174640.png)

![](https://gitee.com/im0o/photobed/raw/master/img/20200406174642.png)

![](https://gitee.com/im0o/photobed/raw/master/img/20200406174641.png)
