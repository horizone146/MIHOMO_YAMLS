# OneSmart 无订阅 / 无节点模板

基于 [666OS/YYDS](https://github.com/666OS/YYDS) 的 OneSmartPro 智能配置（v26.1.4）精简而来，**不包含任何订阅源与节点信息**。

## 相比原版移除

- `proxy-providers`（订阅源占位符）
- `中转服务` 策略组及 `policy-priority` 权重
- 全部线路特性组（高质量 / 低延迟 / 大带宽 / 低倍率线路）
- 对应的 `BaseProvider`、`BaseFB`、`BaseLB` 锚点

## 保留

- 一键智能 / 7 个地区 Smart 组 / 手动选择 策略组架构
- 全套分流规则（34 个规则集：AI、流媒体、电报、Emby 等）
- DNS（fake-ip + rule-set 过滤）、TUN、嗅探、分地区监听端口

## 使用（Clash Party / Mihomo Party）

1. 不要作为独立配置导入（无节点无法使用）
2. 在「覆写」中新建 YAML 覆写，粘贴本文件内容
3. 将覆写挂载到你的订阅配置上
4. 节点由订阅通过 `include-all` + 名称正则自动注入各地区策略组

## 直链

```
https://raw.githubusercontent.com/horizone146/MIHOMO_YAMLS/main/OneSmart_Config_NoSub.yaml
```

> 原配置作者：[@YYDS666](https://github.com/666OS/YYDS) · 上游合集：[HenryChiao/MIHOMO_YAMLS](https://github.com/HenryChiao/MIHOMO_YAMLS)
