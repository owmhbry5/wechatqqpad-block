# wechatqqpad Block List

屏蔽 **wechatqqpad** 等平板伪装模块可能使用的外部网络连接。

## 覆盖范围

| 类型 | 规则 |
|---|---|
| 域名 | `wxqqpad.netlify.app` |
| 域名 | `pic.wztq.ltd` |
| IP | `119.91.29.9` |

## 使用方法

### Hosts

直接将 [`hosts`](./hosts) 覆盖到系统 `/system/etc/hosts`，或使用支持 hosts 的防火墙工具导入。

### Clash / Mihomo

```yaml
rule-providers:
  wechatqqpad:
    type: http
    behavior: domain
    url: https://raw.githubusercontent.com/owmhbry5/wechatqqpad-block/main/rules/clash.yaml
    path: ./ruleset/wechatqqpad.yaml
    interval: 86400
```

### Surge

```ini
RULE-SET,https://raw.githubusercontent.com/owmhbry5/wechatqqpad-block/main/rules/surge.list,REJECT
```

### Quantumult X

```ini
filter_remote=https://raw.githubusercontent.com/owmhbry5/wechatqqpad-block/main/rules/quantumultx.list, tag=wechatqqpad, force-policy=reject, enabled=true
```

### AdGuard

```
https://raw.githubusercontent.com/owmhbry5/wechatqqpad-block/main/rules/adguard.txt
```

## 说明

本规则集仅用于阻止上述模块的网络连接，不涉及任何正常应用。
